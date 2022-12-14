---
title: Gebeurtenissen configureren
description: Configureer drie gebeurtenissen die vereist zijn voor Journey Optimizer Challenges
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: c7826818-c28a-493b-8aba-9d8a8102336d
source-git-commit: db681243c066911af03b75f045a4dc4a990daa7d
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 5%

---

# Gebeurtenissen configureren

In deze sectie stelt u de drie gebeurtenissen in die vereist zijn voor de praktische oefeningen in de [Journey Optimizer-uitdagingen](/help/challenges/introduction-and-prerequisites.md).

De video bekijken [Gebeurtenissen maken](/help/set-up-journeys/create-events.md) voor richtlijnen over het maken van gebeurtenissen.

## Online koopgebeurtenis voor Luma maken

1. Navigeer van de linkernavigatie naar [!UICONTROL ADMINISTRATIE] en selecteert u *[!UICONTROL Configuratie]*
1. Van de [!UICONTROL Dashboard], selecteert u *[!UICONTROL Beheren*]* Gebeurtenissen

![Gebeurtenissen beheren](assets/create-events.png)

1. Klikken *[!UICONTROL Gebeurtenis maken]*
1. Vul de details en parameters van de gebeurtenis in:

   | [!UICONTROL Parameter] | [!UICONTROL Value] |
   |-------------|-----------|
   | [!UICONTROL NAAM] | `LumaOnlinePurchase` |
   | [!UICONTROL TYPE] | [!UICONTROL Unitair] |
   | [!UICONTROL Type gebeurtenis-id] | [!UICONTROL Op regel gebaseerd] |
   | [!UICONTROL Schema] | `Luma Web Events Schema` |
   | [!UICONTROL Velden] | `eventType` <br>`commerce.order.priceTotal`<br>`commerce.order.purchaseOrderNumber`<br>`commerce.shipping.adress.street1`<br>`commerce.shipping.adress.city`<br>`commerce.shipping.adress.postalCode`<br>`commerce.shipping.adress.state`<br>`productListItems.quantity`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.name`<br>`productListItems.Luma Product Catalog Schema._your Organization_IDprice`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.imageURL`<br>`productListItems.Luma Product Catalog Schema._your Organization_ID.url` |

1. Voeg de [!UICONTROL Voorwaarde van gebeurtenis-id]: `LumaOnlinePurchase.eventType is commerce.purchases`

   1. Selecteer het potloodpictogram om het veld te bewerken
   2. Op de [!UICONTROL Voorwaarde voor een gebeurtenis-id toevoegen] modal, slepen en neerzetten `eventType` op het canvas
   3. Selecteer `commerce.purchases`
   4. OK selecteren op het canvas
   5. OK selecteren op het modaal

![Gebeurtenisvoorwaarde toevoegen](/help/tutorial-configure-a-training-sandbox/assets/Event-lumaOnlinePurchase-condition-1.png)

1. Selecteren [!UICONTROL NAMESPACE]: `Luma CRM ID (lumaCrmId)`

2. Selecteren **[!UICONTROL Opslaan]**.

## Maken *[!DNL Luma Wishlist Add]* Gebeurtenis

| [!UICONTROL Parameter] | [!UICONTROL Waarde] |
|-------------|-----------|
| [!UICONTROL NAAM] | `LumaWishlistAdd` |
| [!UICONTROL TYPE] | [!UICONTROL Unitair] |
| [!UICONTROL Type gebeurtenis-id] | [!UICONTROL Op regel gebaseerd] |
| [!UICONTROL Schema] | `Luma Product Interactions` |
| [!UICONTROL Velden] | EventType<br>productListItem.quantity<br><b>In de Punten van de Lijst van het Product > Lumatieproducten > _*[!DNL yourOrganizationID]* > Product:</b> <br>Naam<br>Prijs<br> ProductImageURL<br>ProductURL |
| [!UICONTROL Condition] | [!DNL LumaWishlistAdd.eventType is commerce.saveForLaters] |
| [!UICONTROL Naamruimte] | E-mail (e-mail) |

## Maken *[!DNL Luma Product Restock] Gebeurtenis

| [!UICONTROL Parameter] | [!UICONTROL Waarde] |
|-------------|-----------|
| [!UICONTROL NAAM] | `LumaProductRestock` |
| [!UICONTROL TYPE] | [!UICONTROL Zakelijk] |
| [!UICONTROL Schema] | [!DNL Luma Product Inventory Events] |
| [!UICONTROL Velden] | productID <br> stockEventType<br><b>In product > Luminaproducten > *[!DNL yourOrganizationID]* > Product:</b> <br>Naam<br>Prijs<br> ProductImageURL<br>Beschrijving |
| [!UICONTROL Voorwaarde] | LumaProductRestock._`your organization's ID`.voorraadEvent.stockEventType is restock |

## Gefeliciteerd

Uw sandbox kan nu worden gebruikt!
