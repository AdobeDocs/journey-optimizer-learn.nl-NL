---
title: Impressies en interactiefuncties vastleggen
description: Leg de indruk en interactiegebeurtenissen vast en bereid de gegevens voor rapportage binnen Journey Optimizer voor.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
recommendations: noDisplay, noCatalog
last-substantial-update: 2025-07-18T00:00:00Z
jira: KT-18526
exl-id: 7e6014b5-c5a6-467b-8e31-58c5d966464c
source-git-commit: bfeab1e933f2a510506c0ecf911df41e66cb959b
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---

# Impressies en interactiefuncties vastleggen

Om rapportering over aanbiedingsindrukkingen toe te laten en van het besluit van AJO te klikken, moeten de volgende componenten worden gevormd:
>[!NOTE]
>
> Deze eerste vereisten werden reeds voltooid in creeer schema en datasetsectie van het [ vorige leerprogramma ](https://experienceleague.adobe.com/nl/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/create-schema-and-dataset)

## 1. Dataset in Adobe Experience Platform (AEP)

- Een dataset die op een **wordt gebaseerd XDM ExperienceEvent** schema.

Het schema moet een `Web Details` -veldgroep bevatten waarin de pagina-URL, de verwijzende persoon enzovoort worden vastgelegd.

## &#x200B;2. Configuratie gegevensstroom

- A **Datastream** moet in Adobe Experience Platform worden gecreeerd.
- Deze gegevensstroom moet aan de dataset worden verbonden hierboven wordt gevormd om ervoor te zorgen dat alle gebeurtenissen van SDK van het Web behoorlijk in de juiste bestemming worden opgenomen die.

## &#x200B;3. Eigenschap Adobe Experience Platform-tags

- AEP Web SDK extension configured om de gegevensstroom te gebruiken die in de vroegere stap wordt gecreeerd.
- Experience Cloud ID Service geconfigureerd
- Er wordt een gegevenselement met de naam ECID toegevoegd aan de eigenschap
- Geïmplementeerd op de site waar aanbiedingen worden weergegeven.


Om rapportering over aanbiedingsprestaties toe te laten, moet de eerste stap vangen wanneer de aanbiedingen (indrukkingen) worden getoond en wanneer zij (interactie) worden geklikt. Deze gebeurtenissen vormen de basis voor het meten van de betrokkenheid, het berekenen van doorkliksnelheden en het analyseren van de doeltreffendheid van de aanbieding in Adobe Experience Platform.

De alloy(&quot;sendEvent&quot;) functie wordt gebruikt om gebruikersinteracties met aanbiedingen te registreren die door Adobe Journey Optimizer (AJO) worden teruggegeven.

De sendEvent nuttige lading vangt interacties aan door het gebeurtenistype (decisions.propositionDisplay voor beelden of decisions.propositionInteract voor kliks), een unieke gebeurtenis ID, timestamp, en gebruikersidentiteit (identityMap) te omvatten. Het omvat ook de lijst van aanbiedingen (voorstellen) getoond of geklikt, samen met het volgen van tokens om nauwkeurige attributie te verzekeren. Dankzij deze structuur kunnen gepersonaliseerde aanbiedingsprestaties in Adobe Journey Optimizer worden gerapporteerd en geoptimaliseerd.

Er worden twee typen interactiegebeurtenissen vastgelegd:

## Impressiegebeurtenis

Er ontstaat een indruk wanneer een aanbieding op de pagina wordt weergegeven en zichtbaar wordt voor de gebruiker. De gebeurtenis wordt bijgehouden met het gebeurtenistype decisions.propositionDisplay.


```javascript
 alloy("sendEvent", {
            xdm: {
              _id: generateUUID(),
              timestamp: new Date().toISOString(),
              eventType: "decisioning.propositionDisplay",
              identityMap: {
                    ECID: [{
                      id: _satellite.getVar("ECID"),
                      authenticatedState: "authenticated",
                      primary: true
                    }]
                  },
              _experience: {
                decisioning: {
                  propositionEventType: {
                    display: 1
                  },
                    propositionAction: {
                            id: offerId,
                            tokens: [trackingToken]
                  },
                  
                   propositions: window.latestPropositions
                  
                }
              }
            }
          });
        }
```

## Interactie voorstel

Er wordt een interactie opgenomen wanneer een gebruiker op een call-to-action (CTA) binnen de weergegeven aanbieding klikt. De gebeurtenis wordt gevolgd gebruikend het besluit.propositionInteract gebeurtenistype.

```javascript
alloy("sendEvent", {
                xdm: {
                  _id: generateUUID(),
                  timestamp: new Date().toISOString(),
                  eventType: "decisioning.propositionInteract",
                  identityMap: {
                    ECID: [{
                      id: _satellite.getVar("ECID"),
                      authenticatedState: "ambiguous",
                      primary: true
                    }]
                  },
                  _experience: {
                    decisioning: {
                      propositionEventType: {
                        interact: 1
                      },
                      propositionAction: {
                        id: offerId,
                        tokens: [trackingToken]
                      },
                       propositions: window.latestPropositions
                    }
                  }
                }
              })
```

Het opnemen van voorstellen in klik- en impressiefouten is van essentieel belang voor een juiste berichtgeving over aanbiedingen in Adobe Journey Optimizer. Deze voorstellen vertegenwoordigen de nauwkeurige aanbiedingen die aan de gebruiker werden voorgesteld, toestaand Adobe om gebruikersinteractie (bijvoorbeeld, impressies of kliks) terug naar de specifieke besluiten toe te schrijven die door het systeem worden genomen.

Elk aanbod in een voorstel bevat een trackingtoken. Dit is een unieke id die door Adobe wordt gegenereerd. Dit token moet exact worden doorgegeven zoals het is ontvangen — zonder wijziging — in de corresponderende klik- of impressiegebeurtenis. Overeenkomende trackingtokens zorgen ervoor dat Adobe de actie van de gebruiker precies kan koppelen aan het juiste aanbiedingsbesluit, waardoor downstreamrapportage en op AI gebaseerde optimalisatie mogelijk zijn.
