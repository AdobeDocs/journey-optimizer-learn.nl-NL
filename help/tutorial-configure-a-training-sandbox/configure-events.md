---
title: Gebeurtenissen configureren
description: Vorm drie gebeurtenissen die voor de hands-on Uitdagingen van Journey Optimizer worden vereist
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: 4df1bdca81a585f728aa68519aa7ec7cd0c2f014
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 6%

---

# Gebeurtenissen configureren

In deze sectie stelt u de drie gebeurtenissen in die vereist zijn voor de praktische oefeningen in de [Journey Optimizer-uitdagingen](/help/challenges/introduction-and-prerequisites.md).

In de volgende video wordt uitgelegd hoe u gebeurtenissen kunt maken:

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

## Online Luma-aankoopgebeurtenis maken

Wanneer u deze gebeurtenis gebruikt, ontvangt Journey Optimizer informatie wanneer iemand online lumaproducten koopt.

1. Maak een gebeurtenis met de volgende parameters:

   | [!UICONTROL Parameter] | [!UICONTROL Value] |
   |-------------|-----------|
   | [!UICONTROL NAAM] | `LumaOnlinePurchase` |
   | [!UICONTROL TYPE] | [!UICONTROL Unitair] |
   | [!UICONTROL Type gebeurtenis-id] | [!UICONTROL Op regel gebaseerd] |
   | [!UICONTROL Schema] | `Luma Web Events Schema` |
   | [!UICONTROL Velden] | `eventType` <br>`commerce.order.priceTotal`<br>`commerce.order.purchaseOrderNumber`<br>`commerce.shipping.adress.street1`<br>`commerce.shipping.adress.city`<br>`commerce.shipping.adress.postalCode`<br>`commerce.shipping.adress.state`<br>`productListItems.quantity`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.name`<br>`productListItems.Luma Product Catalog Schema._your Organization_IDprice`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.imageURL`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.url` |

1. Voeg de [!UICONTROL Voorwaarde van gebeurtenis-id]: `LumaOnlinePurchase.eventType is commerce.purchases`:

   1. Selecteer het potloodpictogram om het veld te bewerken.

   1. Op de **[!UICONTROL Voorwaarde voor een gebeurtenis-id toevoegen]** modal, slepen en neerzetten `eventType` op het canvas.
   1. Selecteer `commerce.purchases`.
   1. Selecteren **[!UICONTROL OK]** op het canvas.
   1. Selecteren **[!UICONTROL OK]** op het modaal.

   ![Gebeurtenisvoorwaarde toevoegen](/help/tutorial-configure-a-training-sandbox/assets/Event-lumaOnlinePurchase-condition-1.png)

1. Selecteren [!UICONTROL NAMESPACE]: `Luma CRM ID (lumaCrmId)`

1. Selecteren **[!UICONTROL Opslaan]**.

## Maken *[!DNL Luma Wishlist Add]* event

| [!UICONTROL Parameter] | [!UICONTROL Value] |
|-------------|-----------|
| [!UICONTROL NAAM] | `LumaWishlistAdd` |
| [!UICONTROL TYPE] | [!UICONTROL Unitair] |
| [!UICONTROL Type gebeurtenis-id] | [!UICONTROL Op regel gebaseerd] |
| [!UICONTROL Schema] | `Luma Product Interactions` |
| [!UICONTROL Velden] | EventType<br>productListItem.quantity<br><b>In de Punten van de Lijst van het Product > Lumatieproducten > _*[!DNL yourOrganizationID]* > Product:</b> <br>Naam<br>Prijs<br> ProductImageURL<br>ProductURL |
| [!UICONTROL Condition] | [!DNL LumaWishlistAdd.eventType is commerce.saveForLaters] |
| [!UICONTROL Naamruimte] | E-mail (e-mail) |

## Maken *[!DNL Luma Product Restock]* event

| [!UICONTROL Parameter] | [!UICONTROL Value] |
|-------------|-----------|
| [!UICONTROL NAAM] | `LumaProductRestock` |
| [!UICONTROL TYPE] | [!UICONTROL Zakelijk] |
| [!UICONTROL Schema] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL Velden] | SKU <br> stockEventType<br><b> yourOrganizationID > product:</b> <br>name<br>prijs<br> ImageURL<br>beschrijving |
| [!UICONTROL Condition] | LumaProductRestock._`your organization's ID`.voorraadEvent.stockEventType is restock |

Gefeliciteerd! Uw sandbox kan nu worden gebruikt.
