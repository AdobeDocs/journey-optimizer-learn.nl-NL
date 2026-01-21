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
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Frequentiecattering implementeren op Adobe Journey Optimizer (AJO)-aanbiedingen die via AJO-besluitvorming worden geleverd

Deze zelfstudie laat zien hoe u frequentiekoppeling kunt toepassen op aanbiedingen in Adobe Journey Optimizer om te bepalen hoe vaak gebruikers hetzelfde aanbod in de loop der tijd zien.

Door Beslissing.propositionDisplay en decisions.propositionInteract gebeurtenissen door het Web SDK van Adobe te vangen en hen in kaart te brengen aan schema&#39;s XDM in Adobe Experience Platform (AEP), kan Adobe Journey Optimizer aanbiedingsindrukkingen en interactie nauwkeurig volgen, toelatend frequentietoewijzing om te beperken hoe vaak een aanbieding aan een gebruiker wordt getoond.

## Voorwaarden voor deze zelfstudie

Voordat u verdergaat, moet u ervoor zorgen dat u een geldige Adobe Journey Optimizer-campagne hebt met Beslissing die aanbiedingen actief aan een weboppervlak levert.

Deze zelfstudie gaat ervan uit dat de levering al werkt en richt zich uitsluitend op het configureren en valideren van het gedrag voor frequentiecapping.


