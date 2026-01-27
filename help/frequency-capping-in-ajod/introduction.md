---
title: Frequentiecattering implementeren op Adobe Journey Optimizer (AJO)-aanbiedingen die via AJO-besluitvorming worden geleverd
description: Deze zelfstudie breidt een bestaande Adobe Journey Optimizer (AJO)-implementatie uit door ervoor te zorgen dat de frequentie van aanbiedingen die worden aangeboden met behulp van AJO-beslissing, wordt beperkt. Het schetst hoe u indruk- en interactiegebeurtenissen kunt vastleggen die worden gebruikt bij het toewijzen van frequenties.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
exl-id: ae74485f-9ea1-428d-9c07-5db0c5cf93fb
source-git-commit: 441fdbc33486f027c22d1b94e03919c5666ca003
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Frequentiecattering implementeren op Adobe Journey Optimizer (AJO)-aanbiedingen die via AJO-besluitvorming worden geleverd

Deze zelfstudie laat zien hoe u frequentiekoppeling kunt toepassen op aanbiedingen in Adobe Journey Optimizer om te bepalen hoe vaak gebruikers hetzelfde aanbod in de loop der tijd zien.

Dit leerprogramma veronderstelt u reeds opstelling een campagne van AJO door het [ leerprogramma te volgen op het personaliseren van aanbiedingen die op weersomstandigheden ](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/personalizing-offers-with-real-time-weather-data/introduction) worden gebaseerd

Door Beslissing.propositionDisplay en decisions.propositionInteract gebeurtenissen door het Web SDK van Adobe te vangen en hen in kaart te brengen aan schema&#39;s XDM in Adobe Experience Platform (AEP), kan Adobe Journey Optimizer aanbiedingsindrukkingen en interactie nauwkeurig volgen, toelatend frequentietoewijzing om te beperken hoe vaak een aanbieding aan een gebruiker wordt getoond.

## Voorwaarden voor deze zelfstudie

Voordat u verdergaat, moet u ervoor zorgen dat u een geldige Adobe Journey Optimizer-campagne hebt met Beslissing die aanbiedingen actief aan een weboppervlak levert.

Deze zelfstudie gaat ervan uit dat de levering al werkt en richt zich uitsluitend op het configureren en valideren van het gedrag voor frequentiecapping.




