---
title: Soorten publiek maken
description: AJO-soorten publiek maken op basis van de investeringsvoorkeuren van de gebruiker (voorraden, obligaties, cd's)
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
source-git-commit: f970a1780b1bdf717675cd79c98a38ac422a679f
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---


# AJO-soorten publiek maken op basis van de investeringsvoorkeuren van de gebruiker (voorraden, obligaties, cd&#39;s)

In deze zelfstudie leert u hoe u gebruikersvoorkeuren vastlegt via een webformulier, deze gegevens in real-time naar Adobe Experience Platform (AEP) verzendt en gebruikers dynamisch kwalificeert voor doelgroepen op basis van hun selecties. Door Adobe-tags (Launch), de AEP Web SDK (Alloy.js) en Edge Segmentation te combineren, kunt u klanten die geïnteresseerd zijn in Standen, Obligaties of Certificaten van Aanbetaling (CD&#39;s), direct mogelijkheden bieden tot personalisatie.

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

Gebruikers verzenden hun voorkeuren via een webformulier en deze voorkeuren worden via de AEP Web SDK ingenomen met Adobe Launch, waardoor gebruikers in real-time hun kwalificatie kunnen geven.

## Gebruikte gereedschappen

* Adobe Experience Platform (AEP)

* Adobe Experience Platform-tags

* AEP Web SDK (Alloy.js)

* AEP Edge Segmentation

* Een webpagina met een voorkeursformulier





