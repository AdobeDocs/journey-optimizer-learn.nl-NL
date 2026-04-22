---
title: Pushberichten verzenden tijdens een reis
description: De frequentiecorrectie in Adobe Journey Optimizer wordt toegepast op het individuele aanbiedingsniveau en is afhankelijk van het vastleggen van zowel een indruk- als een klikgebeurtenis. Dit vereist het volgen van besluitoning.propositionDisplay en decisions.propositionInteract gebeurtenissen gebruikend het Web SDK van Adobe en het in kaart brengen van hen aan een bijgewerkt schema van de Gebeurtenis van de Ervaring XDM in Adobe Experience Platform.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Pushberichten verzenden tijdens een reis

Het maken van een reis op basis van een prijsdalingsgebeurtenis maakt real-time, gedragsgedreven betrokkenheid met gebruikers mogelijk. In real-world scenario&#39;s, komt deze gebeurtenis typisch van een achterste prijssysteem voort wanneer de prijs van een product wordt bijgewerkt. In deze zelfstudie simuleren we dat gedrag door een aangepaste price.drop-gebeurtenis via de Adobe Data Layer te verzenden met AEP-tags, inclusief productdetails zoals naam en SKU. Deze gebeurtenis wordt in Adobe Experience Platform gegegeten en gebruikt als instaptrigger voor een reis in Adobe Journey Optimizer. Na ontvangst kan de reis onmiddellijk een persoonlijke pushmelding naar in aanmerking komende gebruikers sturen, hen informeren over de prijsdaling en tijdige actie aanmoedigen.

Het maken van een reis met behulp van een aangepaste gebeurtenis gebeurt in de volgende stappen

## Aangepaste gebeurtenissen maken in Journey Optimizer

Meld u aan bij Adobe Journey Optimizer en navigeer naar Beheer → Configurations → Events en selecteer vervolgens Gebeurtenis maken. Maak een nieuwe gebeurtenis met de naam PriceDropEvent en koppel deze aan het gebeurtenisschema SchemaForPushNotification dat eerder in de zelfstudie is gemaakt. Zorg ervoor dat de gebeurteniseigenschappen zijn geconfigureerd zoals wordt weergegeven in de referentieafbeelding.

![ gebeurtenis-eigenschappen ](assets/price-drop-event.png)

Selecteer in het schema de vereiste velden om deze beschikbaar te maken voor personalisatie. Neem met name `Name` en `SKU` op van het object ProductListItems en de id van de identityMap. Deze gebieden zullen dan binnen de verpersoonlijkingsredacteur toegankelijk zijn, toestaand u om dupbericht berichten dynamisch samen te stellen die op de product en gebruikerscontext worden gebaseerd.

## Tageigenschap maken

Deze eigenschap wordt geconfigureerd met de AEP Web SDK, die is verbonden met de WebPushDataStream die eerder in de zelfstudie is gemaakt. Het markeringsbezit luistert naar de price.drop gebeurtenis op de Laag van Gegevens van Adobe en brengt de relevante productdetails in kaart door het ProductListItems gegevenselement bij te werken. Nadat de gegevens zijn voorbereid, wordt een regel in de eigenschap tag geactiveerd en wordt de gebeurtenis price.drop via het web SDK naar AEP verzonden. Deze gebeurtenis fungeert vervolgens als toegangspunt voor een reis in Adobe Journey Optimizer, waardoor pushberichten direct kunnen worden bezorgd op basis van de prijsdaling.



