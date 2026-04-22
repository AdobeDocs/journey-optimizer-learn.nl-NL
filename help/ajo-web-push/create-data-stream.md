---
title: DataStream maken
description: Deze pagina begeleidt u door het creëren van een gegevensstroom in Adobe Experience Platform, die wordt vereist om gegevens van het Web SDK te verzamelen en het naar AEP en Adobe Journey Optimizer te leiden. De gegevensstroom fungeert als de verbinding tussen uw webtoepassing en Adobe-services, waardoor pushabonnementen en gebeurtenisgegevens kunnen worden verwerkt.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# DataStream maken

Een gegevensstroom in Adobe Experience Platform (AEP) doet dienst als eindpunt dat gegevens ontvangt die van het Web SDK worden verzonden. Het leidt deze gegevens aan de gevormde diensten zoals AEP, Adobe Analytics, of Adobe Journey Optimizer. In deze zelfstudie wordt de datastream gebruikt om abonnementsgegevens en price.drop-gebeurtenissen voor webpush naar AEP te verzenden voor activering.

## Gebeurtenisschema maken voor het bijhouden van pushberichten

Maak een nieuw XDM ExperienceEvent-schema met de naam `SchemaForPushNotification` . Voeg de `Push Notification Tracking` - en `Commerce Details` -veldgroepen toe aan dit schema. De velden van de veldgroep Commerce Details worden gebruikt om productinformatie vast te leggen en de gebeurtenis custom price.drop te activeren.

![ gebeurtenis-schema ](assets/event-schema.png)

## Profielschema maken om toestemming van de gebruiker op te slaan

Voor deze zelfstudie gebruiken we de uit-van-de-doos `AJO Push Profile Schema` . In dit schema worden de gegevens van het pushabonnement van de gebruiker opgeslagen, inclusief het pushtoken dat is vereist voor het verzenden van pushberichten via het web.

![ profile_schema ](assets/profile-schema.png)

## Gegevenssets maken voor het schema

Maak een gegevensset met de naam `DataSetForPushNotification` met het eerder gemaakte gebeurtenisschema. Voor profielgegevens gebruikt u de uit-van-de-doos `AJO Push Profile Dataset`, die aan het schema van het duwprofiel wordt geassocieerd. Noteer de id van `DataSetForPushNotification` , zoals later in de zelfstudie wordt vereist wanneer u de toepassing configureert via het .env-bestand.

## Gegevensstroom maken met de gebeurtenis- en profielgegevensset

Creeer een nieuwe gegevensstroom genoemd WebPushDataStream gebruikend de gebeurtenis en profieldatasets die in de vorige stap worden gecreeerd. Noteer de DataStream-id, die later in de zelfstudie wordt vereist wanneer u de toepassing via het .env-bestand configureert.

![ datastream ](assets/datastream.png)
