---
title: Aanbiedingen volgen en rapporteren Adobe Jouney Optimizer (AJO) die via AJO Offer Decisioning worden geleverd
description: Deze zelfstudie breidt een bestaande Adobe Journey Optimizer (AJO)-implementatie uit die persoonlijke aanbiedingen biedt op basis van contextuele gegevens zoals temperatuur. Het schetst hoe u indruk- en interactiegebeurtenissen vastlegt en de gegevens voorbereidt voor rapportage binnen Jouney Optimizer.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
jira: KT-18526
source-git-commit: fa4795d92cf290b867df23277a297c99d6222224
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Trackingtokens toevoegen om objecten aan te bieden

Voer de volgende stappen uit om de code in de personalisatie-editor te wijzigen:

Navigeer aan _&#x200B;**beheer van de Reis ->Campagnes**&#x200B;_

Open de aangewezen campagne en klik de _&#x200B;**campagne van het Einde**&#x200B;_ knoop om de campagne tegen te houden.

Open de tegengehouden campagne en klik op _&#x200B;**wijzigen campagne**&#x200B;_ knoop.

Klik op _&#x200B;**Inhoud**&#x200B;_ lusje en klik dan op _&#x200B;**geef code**&#x200B;_ knoop uit om de verpersoonlijkingsredacteur te openen.

Twee nieuwe gegevenskenmerken aan de div toevoegen, zoals wordt weergegeven in de schermafbeelding
![&#x200B; het volgen-teken &#x200B;](assets/offer-item-with-tracking-code.png)

TrackingToken en ItemID kunnen worden toegevoegd door op het pictogram van het Beleid van het Besluit in de linkernavigatie te klikken en onderaan de beslissingsboom te boren itemID en trackingToken te selecteren.
![&#x200B; het volgen-teken &#x200B;](assets/insert-tracking-token.png)

Op deze manier zorgt u ervoor dat elk gerenderde aanbod een token voor het bijhouden van gegevens bevat. Dit is essentieel voor een nauwkeurige indruk en het bijhouden van gebeurtenissen.

Sla de wijzigingen op en activeer de campagne.
