---
title: XDM-schema, gegevensset en gegevensstroom instellen in AEP
description: XDM-schema's, gegevensset en gegevensstroom maken
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: 1c7fe9e7-ab72-4d7b-960a-512d0e25808b
source-git-commit: 319b1cd4a037807a944e5fb6438e47b5fcf4c1c4
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# XDM-schema, gegevensset en gegevensstroom instellen in AEP

## XDM-schema maken

Om Adobe Experience Platform Web SDK (Alloy.js) op een Web-pagina te gebruiken, moeten de Markeringen van AEP met een Datasstream worden geassocieerd die aan een XDM- Gebeurtenisschema in kaart wordt gebracht. Het Web SDK (alloy.sendEvent) verzendt gegevens naar AEP als Gebeurtenissen van de Ervaring, die met een schema moeten in overeenstemming zijn XDM dat op de klasse XDM ExperienceEvent wordt gebaseerd.

Een XDM-schema maken

- Aanmelden bij Adobe Experience Platform
- Navigeer aan _&#x200B;**Gegevensbeheer -> Schema&#39;s -> creeer schema**&#x200B;_

- Creeer een XDM gebeurtenis gebaseerd schema genoemd **_Weer-Schema_**. Als u niet vertrouwd met het creëren van een schema bent, te volgen gelieve deze [&#x200B; documentatie &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/tutorials/create-schema-ui)


- Zorg ervoor dat het schema de volgende gebieden met aangewezen gegevenstype heeft.

- ![&#x200B; weer-schema &#x200B;](assets/weather-schema.png)

- Voeg de Details van het Web van de Groep van het Gebied _&#x200B;**aan het schema toe.**&#x200B;_ Deze veldgroep is vereist voor rapportagedoeleinden.

## Creeer een Dataset die op het Schema wordt gebaseerd

A **dataset in Adobe Experience Platform (AEP)** is een gestructureerde opslagcontainer die wordt gebruikt om, gegevens in te voeren op te slaan en te activeren die op een bepaald schema XDM worden gebaseerd.

- Navigeer aan _&#x200B;**Gegevensbeheer -> Datasets -> Create dataset**&#x200B;_
- Creeer een dataset genoemd **_Weer-schema-dataset_** die op het XDM schema (_&#x200B;**wordt gebaseerd Weer-Schema**&#x200B;_) in de vorige stap wordt gecreeerd.


## Een DataStream maken

Een gegevensstroom in Adobe Experience Platform is vergelijkbaar met een beveiligde pijplijn (of snelweg) die uw website of toepassing verbindt met Adobe-services, waardoor gegevens kunnen worden ingevoerd en inhoud op maat kan worden teruggestroomd.

- Navigeer aan _&#x200B;**de Inzameling van Gegevens > Gegevensstromen**&#x200B;_, dan klik Nieuwe DataStream. Noem de datastream **weer-verwant-datastream**


- Geef de volgende details op, zoals hieronder in de schermafbeelding wordt weergegeven
  ![&#x200B; datastream &#x200B;](assets/datastream.png)
- Klik op Opslaan, klik vervolgens op Toewijzing toevoegen en voeg de Adobe Experience Platform-service en de Dataset van de gebeurtenis toe met de desbetreffende selectievakjes ingeschakeld
  ![&#x200B; datastream-afbeelding &#x200B;](assets/datastream-service.png)

- Sla de gegevensstroom op.


>[!NOTE]
>
>Opmerking: nieuwe gegevenssets kunnen maximaal 24 uur duren voordat ze beschikbaar zijn voor selectie in de Beoordelingsformule of de Personalization-editor.
