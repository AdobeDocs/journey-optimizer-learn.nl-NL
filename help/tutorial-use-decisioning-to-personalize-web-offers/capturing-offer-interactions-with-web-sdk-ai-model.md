---
title: Interacties met het vastlegaanbod met Adobe Web SDK for AI-modeltraining
description: Dit artikel richt zich op het vastleggen van gebruikersinteractiegegevens—zoals aanbiedingsindrukkingen en klikken—met behulp van Adobe Experience Platform Web SDK (alloy.js). Deze gegevens dienen als basis voor het trainen van AI-modellen in Adobe Journey Optimizer (AJO) om aanbiedingen op intelligente wijze te rangschikken op basis van gebruikersgedrag en contextuele signalen.
feature: Decisioning
topic: Integrations
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2025-07-08T00:00:00Z
jira: KT-18451
source-git-commit: dfb280df3453e7811dffd95b9af664b873a9af31
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---


# Interacties met het vastlegaanbod met Adobe Web SDK for AI-modeltraining

In dit artikel wordt getoond hoe u aanbiedingsinteractiegebeurtenissen (zoals indrukken of klikken) vastlegt met de Adobe Experience Platform Web SDK door legering (&quot;sendEvent&quot;, ...) rechtstreeks in uw JavaScript-code aan te roepen. De gegevens worden in AEP ingevoerd en gebruikt om AI-modellen in Adobe Journey Optimizer (AJO) op te leiden voor een slimmer aanbod op basis van real-time gedrag.

## Vereisten

Controleer voordat u begint of het volgende is ingesteld:

- Een werkende Adobe Launch-eigenschap met de Adobe Experience Platform Web SDK-extensie geïnstalleerd.

- A [&#x200B; datastream &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/decisioning/experience-decisioning/collect-event-data/create-dataset) gevormd en in kaart gebracht aan uw zandbak van AEP.

- Een website waarop Starten wordt geïmplementeerd.


## Schema en Dataset maken voor Interactie Gebeurtenissen aanbod

Om ervaringsgebeurtenissen te verzamelen, moet u eerst een dataset tot stand brengen waar deze gebeurtenissen zullen worden verzonden.

Volg de stappen in dit [&#x200B; worden vermeld artikel om het vereiste schema en de dataset &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/decisioning/experience-decisioning/collect-event-data/create-dataset) tot stand te brengen die

## Een gegevensstroom maken in AEP

![&#x200B; gegeven-stroom &#x200B;](assets/ai-model-data-stream.png)
Adobe Experience Platform Service toevoegen aan de gegevensstroom
![&#x200B; gegeven-stroom-dienst &#x200B;](assets/data-stream-service.png)

## Adobe Experience Platform-tag configureren met Web SDK

In de extensie-instellingen:

Adobe Experience Platform Web SDK-extensie configureren voor het gebruik van de gemaakte DataStream
