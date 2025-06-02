---
title: XDM-schema, gegevensset en gegevensstroom instellen in AEP
description: XDM-schema's, gegevensset en gegevensstroom maken
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-18089
source-git-commit: 860f4fa4f6b491f3327776ba372bd5fa20e5d5d3
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# XDM-schema, gegevensset en gegevensstroom instellen in AEP

## XDM-schema maken

Om Adobe Experience Platform Web SDK (Alloy.js) op een Web-pagina te gebruiken, moeten de Markeringen van AEP met een Datasstream worden geassocieerd die aan een XDM- Gebeurtenisschema in kaart wordt gebracht. Het Web SDK (alloy.sendEvent) verzendt gegevens naar AEP als Gebeurtenissen van de Ervaring, die met een schema moeten in overeenstemming zijn XDM dat op de klasse XDM ExperienceEvent wordt gebaseerd.

Een XDM-schema maken

* Aanmelden bij Adobe Experience Platform
* Gegevensbeheer -> Schema&#39;s -> Schema maken

* Creeer een XDM gebeurtenis gebaseerd schema genoemd **_Financiële Advisors_**. Als u niet vertrouwd met het creëren van een schema bent, te volgen gelieve deze [ documentatie ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/tutorials/create-schema-ui)


* Controleer of het schema is ingeschakeld voor het profiel.

## Creeer een Dataset die op het Schema wordt gebaseerd

A **dataset in Adobe Experience Platform (AEP)** is een gestructureerde opslagcontainer die wordt gebruikt om, gegevens in te voeren op te slaan en te activeren die op een bepaald schema XDM worden gebaseerd.


* Gegevensbeheer -> Datasets -> Gegevensset maken
* Creeer een dataset genoemd **_de gegevensreeks van Advisors van de Financiële_** die op het schema XDM (Financiële Advisors) wordt gebaseerd die in de vorige stap wordt gecreeerd.

* Zorg ervoor dat de dataset voor profiel wordt toegelaten

## Een DataStream maken

Een gegevensstroom in Adobe Experience Platform is vergelijkbaar met een beveiligde pijplijn (of snelweg) die uw website of toepassing verbindt met Adobe-services, waardoor gegevens kunnen worden ingevoerd en inhoud op maat kan worden teruggestroomd.

* Navigeer naar Gegevensverzameling > Gegevensstromen en klik vervolgens op Nieuwe gegevensstroom. Noem de datastream **_Financiële Advisors DataStream_**

* Geef de volgende details op, zoals hieronder in de schermafbeelding wordt weergegeven
  ![ datastream ](assets/datastream.png)
* Klik op Opslaan, klik vervolgens op Toewijzing toevoegen en voeg de Adobe Experience Platform-service en de Dataset van de gebeurtenis toe zoals deze worden weergegeven
  ![ datastream-afbeelding ](assets/datastream-service.png)

* Kies de aangewezen (vroeger gecreeerd) dataset van de gebeurtenisdataset.

* Sla de gegevensstroom op.

