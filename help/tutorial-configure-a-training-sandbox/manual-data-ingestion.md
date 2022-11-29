---
title: Gegevens handmatig verzamelen
description: Maak gegevenssets en voeg handmatig voorbeeldgegevens in.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: 5e7bf81d-4d70-48ef-b357-c361b28359db
source-git-commit: 8a2062f0719e799dd2d039488e6bba943fb458c4
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 6%

---

# Gegevens handmatig verzamelen

Deze sectie begeleidt u door de vereiste stappen om gegevensreeksen tot stand te brengen en steekproefgegevens in te voeren.

>[!TIP]
>
> De videozelfstudie bekijken [Gegevenssets maken en gegevens opnemen](/help/set-up-data/create-datasets-and-ingest-data.md) voordat u begint.

U maakt vijf [!UICONTROL gegevenssets] gebaseerd op de Luma [!UICONTROL schema&#39;s] u in [vorige sectie](/help/tutorial-configure-a-training-sandbox/manual-data-set-up.md). Nadat de datasets zijn gecreeerd, kunt u gegevens van de JSON dossiers ingaan u downloadde en veranderde. (Zie [Inleiding en voorwaarden](/help/tutorial-configure-a-training-sandbox/introduction-and-prerequisites.md) voor instructies).

## De eerste gegevensset maken

Een gegevensset maken met de naam *[!DNL Luma Loyalty Data]* van [!DNL Luma Loyalty schema]

1. Van de linkernavigatie, onder [!UICONTROL GEGEVENSBEHEER], selecteert u **[!UICONTROL Gegevenssets]**.

1. Selecteren **[!UICONTROL Gegevensset maken]**.

   ![Een gegevensset maken](assets/create-dataset.png)

1. Selecteer op de volgende pagina de optie [!UICONTROL Gegevensset maken van schema].

   ![Een gegevensset maken op basis van een schema](assets/create-dataset-from-schema.png)

1. Zoek op de volgende pagina naar de *[!DNL Luma Loyalty]* schema dat u eerder hebt gemaakt.

1. Selecteer *[!DNL Luma Loyalty]*.

1. Klik op **[!UICONTROL Next]**.

   ![Schema zoeken en selecteren](assets/create-dataset-select-schema.png)

1. Vorm de dataset:

   * Naam: `Luma Loyalty Data`

1. Klikken **[!UICONTROL Voltooien]**.

   ![Gegevensset configureren](assets/create-dataset-configure.png)

## Voorbeeldgegevens samenvoegen

Na het creëren van een dataset, kunt u gegevens in de dataset opnemen.

1. Op de [!DNL Luma Loyalty Data] pagina, omlaag schuiven naar de onderkant van het rechterdeelvenster [!UICONTROL GEGEVENS TOEVOEGEN] en inschakelen:

   * **[!UICONTROL Foutdiagnostiek]** en

   * **[!UICONTROL Gedeeltelijke inname]**

   ![Gegevens samenvoegen](assets/ingest-data.png)

1. Sleep de `luma-loyalty.json` bestand om voorbeeldgegevens naar de gegevensset te uploaden.

1. Vernieuw de pagina en controleer de batchstatus om te controleren of het bestand correct is ingevoerd.

   375 records hadden moeten worden ingenomen. Het kan een paar minuten duren voordat de gegevens worden ingevoerd.

>[!TIP]
>
>Als de batch mislukt, moet u ervoor zorgen dat u de organisatie-id hebt vervangen in het dialoogvenster `luma-loyalty.json` bestand met uw [organisatie-id](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=nl).

## Vijf extra maken [!UICONTROL gegevenssets]

Maak vervolgens de volgende vijf extra [!UICONTROL gegevenssets] en de gegevens in de `Luma CRM Data`de `Luma Products Data`en de `Luma Test Profiles` gegevenssets.

| Naam gegevensset | Van schema | In te voeren bestand | Records |
| -----| ------ | -------| ------- |
| `Luma CRM Data` | `Luma CRM` | `luma-crm.json` | 500 |
| `Luma Products Data` | `Luma Products` | `luma-products.json` | 92 |
| `Luma Product Interactions Data` | `Luma Product Interactions` | none | 0 |
| `Luma Product Inventory Events` | `Luma Product Inventory Events` | none | 0 |
| `Luma Test Profiles` | `Luma Test Profiles` | `luma-test-profiles.json` | 3 |

## Volgende stappen

U hebt alle vereiste gegevenssets gemaakt en de voorbeeldgegevens opgenomen. De laatste stap is: [gebeurtenissen configureren](/help/tutorial-configure-a-training-sandbox/configure-events.md).
