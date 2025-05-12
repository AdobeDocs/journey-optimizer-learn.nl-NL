---
title: XDM-schema, gegevensset en gegevensstroom instellen in AEP
description: XDM-schema's, gegevensset en gegevensstroom maken
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
exl-id: 0efa418a-5b4f-4012-a6fc-afaa34a59285
source-git-commit: 15b2379c251ed0d7583a01fb6af67815322456cf
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# XDM-schema, gegevensset en gegevensstroom instellen in AEP

## XDM-schema maken

* Aanmelden bij Adobe Experience Platform
* Gegevensbeheer -> Schema&#39;s -> Schema maken

* Creeer een XDM gebeurtenis gebaseerd schema genoemd _Financiële Advisors_. Als u niet vertrouwd met het creëren van een schema bent, te volgen gelieve deze [ documentatie ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/tutorials/create-schema-ui)

* Voeg de volgende structuur aan uw schema toe. In het PreferredFinancialInstrument-element wordt de voorkeur van de gebruiker voor Stocks, Bonds, CD opgeslagen. **__techmarketingdemos_**&#x200B;is huurder identiteitskaart, en zal in uw milieu verschillend zijn.
  ![ xdm-schema ](assets/xdm-schema.png)

* Het PreferredFinancialInstrument-element heeft opsommingswaarden die hieronder zijn gedefinieerd
  ![ enum-waarden ](assets/enum-values.png)

* Controleer of het schema is ingeschakeld voor het profiel.

## Creeer een Dataset die op het Schema wordt gebaseerd

A **dataset in Adobe Experience Platform (AEP)** is een gestructureerde opslagcontainer die wordt gebruikt om, gegevens in te voeren op te slaan en te activeren die op een bepaald schema XDM worden gebaseerd.


* Gegevensbeheer -> Datasets -> Gegevensset maken
* Creeer een dataset genoemd _de gegevensreeks van Advisors van de Financiële_ die op het schema XDM (Financiële Advisors) wordt gebaseerd die in de vorige stap wordt gecreeerd.

* Zorg ervoor dat de dataset voor profiel wordt toegelaten

## Een DataStream maken

Een gegevensstroom in Adobe Experience Platform is vergelijkbaar met een beveiligde pijplijn (of snelweg) die uw website of toepassing verbindt met Adobe-services, waardoor gegevens kunnen worden ingevoerd en inhoud op maat kan worden teruggestroomd.

* De Inzameling van gegevens > gegevensstromen, dan klik Nieuwe Datasstream. Noem de datastream _Financiële Advisors DataStream_

* Geef de volgende details op, zoals hieronder in de schermafbeelding wordt weergegeven
  ![ datastream ](assets/datastream.png)
* Klik op Opslaan, klik vervolgens op Toewijzing toevoegen en voeg de Adobe Experience Platform-service en de Dataset van de gebeurtenis toe zoals deze worden weergegeven
  ![ datastream-afbeelding ](assets/datastream-service.png)

* Kies de aangewezen (vroeger gecreeerd) dataset van de gebeurtenisdataset.

* De gegevensstroom opslaan

