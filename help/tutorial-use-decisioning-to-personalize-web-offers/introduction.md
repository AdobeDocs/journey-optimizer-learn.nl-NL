---
title: Webaanbiedingen personaliseren met beslissing
description: Leer hoe u Journey Optimizer (AJO) Decisioning kunt gebruiken om persoonlijke aanbiedingen op een webpagina te leveren door gebruik te maken van de segmentering van het publiek die is ingebouwd in Experience Platform (AEP).
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 382ee746-e8cd-4843-bfe9-913df8914136
source-git-commit: 0c42bf9a9af53bf80a14d904733ae0c1f03be0ee
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Beslissing gebruiken om webaanbiedingen aan te passen

Deze zelfstudie bouwt verder op een eerder gemaakte configuratie voor publiekssegmentatie met behulp van Adobe Experience Platform (AEP) Web SDK. In het [ vorige leerprogramma ](https://experienceleague.adobe.com/nl/docs/journey-optimizer-learn/create-audiences-using-web-sdk/introduction), gebruiker voorkeur-zulke zoals rente in Voorraden, Obligaties, of Certificaten van Deposito (CDs)-werd gevangen en gebruikt om individuen in gericht publiek binnen Adobe Experience Platform (AEP) te segmenteren. Deze zelfstudie bouwt verder op die basis door Adobe Journey Optimizer (AJO) Decisioning te gebruiken om persoonlijke financiële aanbiedingen te leveren aan die doelgroepen in real-time, waardoor zowel de betrokkenheid als de conversiesultaten worden verbeterd.

Met de onderstaande link kun je de persoonlijke aanbiedingen van AJO live testen.
[ klik hier om de levende manifestatie ](https://gbedekar489.github.io/finwise/welcome.html) te bekijken — de pagina zal aanbiedingen in real time tonen die op uw investeringsvoorkeur worden gebaseerd.

## Voorwaarden voor deze zelfstudie

* Toegang tot Adobe Experience Platform

* Basiskennis van Adobe Experience Platform-concepten (profielen, soorten publiek, gegevenssets)

* Kennis van Adobe Journey Optimizer

* Basiskennis van JavaScript (eenvoudige functies lezen en schrijven)

* Mogelijkheid om Browser DevTools te gebruiken (tabbladen Console en Netwerk)


## Goal

Deze zelfstudie begeleidt u door het aanbieden van persoonlijke investeringsaanbiedingen (zoals voorraden, obligaties of cd&#39;s) op een website met Adobe Journey Optimizer (AJO). Door gebruik te maken van segmentatie van het publiek en beslissingsstrategieën, leert u hoe u ervoor kunt zorgen dat elke bezoeker het meest relevante aanbod ziet op basis van zijn voorkeuren.

## Gebruikte gereedschappen

* Adobe Experience Platform (AEP)
* Adobe Journey Optimizer (AJO)
* Adobe Experience Platform-tags
* AEP Web SDK (Alloy.js)
* AEP Edge Segmentation
* Een webpagina waarop de aanbiedingen worden weergegeven
