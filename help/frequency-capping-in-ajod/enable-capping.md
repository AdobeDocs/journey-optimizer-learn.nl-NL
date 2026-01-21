---
title: Frequentiecapping inschakelen voor een AJO-campagne
description: De frequentiecorrectie in Adobe Journey Optimizer wordt toegepast op het individuele aanbiedingsniveau en is afhankelijk van het vastleggen van zowel een indruk- als een klikgebeurtenis. Dit vereist het volgen van besluitoning.propositionDisplay en decisions.propositionInteract gebeurtenissen gebruikend het Web SDK van Adobe en het in kaart brengen van hen aan een bijgewerkt schema van de Gebeurtenis van de Ervaring XDM in Adobe Experience Platform.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-18526
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Frequentiecapping inschakelen voor een AJO-campagne

Voer de volgende stappen uit om de frequentiecontrole toe te passen op aanbiedingen:

## Het gebeurtenisschema bijwerken

* Het bestaande gebeurtenisschema bijwerken door de veldgroep toe te voegen zoals wordt weergegeven
* ![&#x200B; gebeurtenis-schema &#x200B;](assets/schema.png)

## Update de frequentie die voor de aanbieding wordt begrensd


* ![&#x200B; aanbieding &#x200B;](assets/offer-capping.png)

## Trackingtoken toevoegen aan de aanbieding

Bewerk het beslissingsbeleid dat in de campagne wordt gebruikt door een fallback-aanbieding toe te voegen
![&#x200B; fallback &#x200B;](assets/fallback.png)

TrackingToken en ItemID kunnen worden toegevoegd door op het pictogram van het Beleid van het Besluit in de linkernavigatie te klikken en onderaan de beslissingsboom te boren itemID en trackingToken te selecteren.

Voeg de item-id en de trackingtoken toe aan de div die het aanbod bevat, zoals hieronder wordt weergegeven
![&#x200B; identiteitskaart-en-volgen-teken &#x200B;](assets/id-and-tracking-token.png)

Op deze manier zorgt u ervoor dat elk gerenderde aanbod een token voor het bijhouden van gegevens bevat. Dit is essentieel voor een nauwkeurige indruk en het bijhouden van gebeurtenissen.


Activeer de gewijzigde campagne.


## Afbeeldings- en volggebeurtenissen verzenden

Wijzig de bestaande JavaScript-code om met behulp van de Adobe Web SDK indruk- en interactiegebeurtenissen vast te leggen en te verzenden. Verwijs naar de [&#x200B; hier verstrekte steekproefcode.](capture-impression-click-events.md)


