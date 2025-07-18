---
title: Adobe Journey Optimizer (AJO)-aanbiedingen volgen en rapporteren via AJO Offer Decisioning
description: Deze zelfstudie breidt een bestaande Adobe Journey Optimizer (AJO)-implementatie uit die persoonlijke aanbiedingen biedt op basis van contextuele gegevens zoals temperatuur. Het schetst hoe u indruk- en interactiegebeurtenissen vastlegt en de gegevens voorbereidt voor rapportage binnen Journey Optimizer.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00Z
jira: KT-18526
source-git-commit: 23832f2e59ca7558fd403f0a9753db3923023e6d
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Adobe Journey Optimizer (AJO)-aanbiedingen volgen en rapporteren via AJO Offer Decisioning

Dit gebruiksscenario is gericht op het mogelijk maken van rapportage en prestatieanalyse voor aanbiedingen die via Adobe Journey Optimizer (AJO) worden geleverd. Wanneer aanbiedingen worden gepersonaliseerd en geleverd op basis van contextuele signalen (zoals weer of locatie), is het van essentieel belang dat zowel impressies als gebruikersinteracties worden bijgehouden om de effectiviteit ervan te evalueren.

Door Beslissing.propositionDisplay en decisions.propositionInteract gebeurtenissen via het Web SDK van Adobe te vangen en hen in kaart te brengen aan gestructureerde schema&#39;s XDM in Adobe Experience Platform (AEP), worden de aanbod-vlakke betrokkenheidsgegevens beschikbaar voor analyse. Deze gegevens kunnen vervolgens in Customer Journey Analytics (CJA) worden gebruikt om dashboards te bouwen, belangrijke metriek zoals klik-door tarief (CTR) te meten, en aanbiedingsprestaties over verschillende publiekssegmenten en contextafhankelijke voorwaarden te vergelijken.

Het doel is duidelijke, op gegevens gebaseerde inzichten te verschaffen in de manier waarop gepersonaliseerde aanbiedingen presteren en toekomstige beslissingsstrategieën te ondersteunen.




![ rapporterend-dashboard ](assets/dashboard-reporting.png)



## Voorwaarden voor deze zelfstudie

Alvorens te beginnen, voltooi de [ Persoonlijke Aanbiedingen met het Echte - de leerprogramma van Gegevens van het Echte - tijdGegevens.](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction) Alle basiscomponenten worden ingesteld, waaronder:

- Web SDK-integratie

- Aanbiedingsinstellingen in Adobe Journey Optimizer (AJO)

- Beslissing met gebruik van contextafhankelijke kenmerken zoals weer en temperatuur

- Rendering in realtime aanbiedingen op een webpagina

Deze zelfstudie bouwt rechtstreeks voort op die implementatie en richt zich specifiek op het vastleggen van aanbiedingsindrukken en interacties voor rapportage en analyse in Journey Optimizer.

