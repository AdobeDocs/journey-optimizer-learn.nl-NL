---
title: Soorten publiek maken met Web SDK
description: In deze zelfstudie leert u hoe u gebruikersvoorkeuren vastlegt via een webformulier, deze gegevens in real-time naar Adobe Experience Platform (AEP) verzendt en gebruikers dynamisch kwalificeert voor doelgroepen op basis van hun selecties. Door Adobe-tags (Launch), de AEP Web SDK (Alloy.js) en Edge Segmentation te combineren, kunt u klanten die geïnteresseerd zijn in voorraden, obligaties of certificaten van aanbetaling (CD's) direct mogelijkheden bieden voor personalisatie.
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
exl-id: ebaa3aa5-0a08-43fd-8d06-8e4b5d8dee05
source-git-commit: 163edfb3367d03729d68c9339ee2af4a0fe3a1b3
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Soorten publiek maken met Web SDK

In deze zelfstudie leert u hoe u gebruikersvoorkeuren vastlegt via een webformulier, deze gegevens in real-time naar Adobe Experience Platform (AEP) verzendt en gebruikers dynamisch kwalificeert voor doelgroepen op basis van hun selecties. Door Adobe-tags (Launch), de AEP Web SDK (Alloy.js) en Edge Segmentation te combineren, kunt u klanten die geïnteresseerd zijn in voorraden, obligaties of certificaten van aanbetaling (CD&#39;s) direct mogelijkheden bieden voor personalisatie.

## Voorwaarden voor deze zelfstudie

* Toegang tot Adobe Experience Platform

* Basiskennis van Adobe Experience Platform-concepten (profielen, soorten publiek, gegevenssets)

* Kennis van Adobe-tags (Launch) — Data Elements en Rules instellen

* Basiskennis van JavaScript (eenvoudige functies lezen en schrijven)

* Mogelijkheid om browser DevTools (de lusjes van de Console en van het Netwerk) te gebruiken


## GOAL

Deze zelfstudie heeft tot doel drie verschillende soorten publiek in Adobe Experience Platform (AEP) op te bouwen en te kwalificeren:

* Klanten die geïnteresseerd zijn in voorraden

* Klanten die geïnteresseerd zijn in obligaties

* Klanten die geïnteresseerd zijn in cd&#39;s

Gebruikers verzenden hun voorkeuren via een webformulier. Deze voorkeuren worden via de AEP Web SDK ingevoerd met Adobe Launch, zodat gebruikers in real-time hun kwalificatie kunnen opgeven.

## Gebruikte gereedschappen

* Adobe Experience Platform (AEP)

* Adobe Experience Platform-tags

* AEP Web SDK (Alloy.js)

* AEP Edge Segmentation

* Een webpagina met een voorkeursformulier
