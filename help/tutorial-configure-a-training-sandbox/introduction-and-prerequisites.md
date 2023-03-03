---
title: Een trainingssandbox configureren - inleiding
description: Leer hoe u een sandbox configureert voor trainingsdoeleinden. Ga door de stappen die worden vereist om de schema's te vormen, steekproefgegevens in te voeren, en gebeurtenissen tot stand te brengen.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 8fa673de-9be9-4ab2-94cf-cfa8ac518223
source-git-commit: f7bfe367411f2bae23631ac4ecb34ad1d250381c
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 5%

---

# Een trainingssandbox configureren - Inleiding en voorwaarden

![Bannerzelfstudie - Een trainingssandbox configureren](./assets/ajo-banner-configure-training-sandbox.png)

Deze zelfstudie is bedoeld voor beheerders en gegevensengineers die een Adobe moeten leveren [!DNL Journey Optimizer] opleidingsomgeving. Leer de stappen die worden vereist om de schema&#39;s te vormen, steekproefgegevens in te voeren, en gebeurtenissen tot stand te brengen. U maakt ook drie testprofielen waarmee de studenten hun werk kunnen controleren.

De verstrekte voorbeeldgegevens zijn gebaseerd op een fictieve atletiekonderneming, genaamd: _[!DNL Luma]_. [!DNL Luma] bevat winkels in meerdere landen, een online aanwezigheid met een website en mobiele apps. [!DNL Luma] gebruikt Adobe Journey Optimizer om verbonden, contextafhankelijke en gepersonaliseerde ervaringen aan hun klanten te bieden.

Aan het einde van deze zelfstudie hebt u een sandbox die de [!DNL Luma] gebruik van gevallen die in de praktische oefeningen in de [Journey Optimizer-uitdagingen](/help/challenges/introduction-and-prerequisites.md) sectie.

## Vereisten

Voordat u begint met het instellen van de trainingssandbox, moet u controleren of:

1. Een speciale ontwikkeling [sandbox](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/access-control/create-and-manage-sandboxes.html?lang=en).

1. [Voorinstellingen voor e-mailberichten](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/set-up-email-channel.html?lang=en) geconfigureerd voor marketing en transactieberichten.

1. **[!UICONTROL Reisbeheerder]** en **[!UICONTROL Data Manager]** rechten voor de trainingssandbox.

1. Uw [organisatie-id](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=nl).

1. De JSON-bestanden met de voorbeeldgegevens, geconfigureerd voor uw Journey Optimizer-instantie:

   1. Download de `luma-sample-data.zip` file [hier](/help/tutorial-configure-a-training-sandbox/assets/luma-data/luma-sample-data.zip), die alle JSON-bestanden bevat die voor deze zelfstudie zijn vereist.

   1. Verplaats vanuit de downloadmap de `luma-data.zip` naar de gewenste locatie op de computer en decomprimeer het bestand.

      Deze bestanden bevatten de voorbeeldgegevens voor uw trainingssandbox.

   1. Elk bestand openen en zoeken **`yourOrganizationID`** en vervang het door uw [organisatie-id](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=nl).

   1. Sla de bestanden op.

## Laten we aan de slag gaan

Beginnen met de [Handmatige gegevensinstelling](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md).

In deze stap definieert u de vereiste gegevensstructuur. Nadat u de gegevensset hebt voltooid, kunt u gegevens in uw sandbox invoeren en vervolgens gebeurtenissen instellen.
