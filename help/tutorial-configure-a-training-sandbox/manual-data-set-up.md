---
title: Gegevensstructuur handmatig instellen
description: Maak de vereiste naamruimten en definieer de gegevensstructuur van het Luminagevoorbeeld.
feature: Sandboxes, Data Management, Application Settings
doc-type: tutorial
kt: 9382
role: Admin
level: Beginner
recommendations: noDisplay, noCatalog
exl-id: de870229-d9a6-4051-9f76-13d402cce3b4
source-git-commit: 8a2062f0719e799dd2d039488e6bba943fb458c4
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 2%

---

# Gegevens handmatig instellen

In deze sectie maakt u de vereiste naamruimten en definieert u de [!DNL Luma] de structuur van steekproefgegevens door te creëren [[!UICONTROL schema&#39;s]](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html).

>[!TIP]
>De videozelfstudie bekijken [Identiteiten toewijzen](/help/set-up-data/map-identities.md) voordat u begint.

## Stap 1: Naamruimten voor identiteiten maken

In deze stap maakt u naamruimten voor de [!DNL Luma] aangepaste identiteitsvelden genaamd `loyaltyId`, `crmId`, en `lumaProduct`. Identiteitsnaamruimten spelen een kritieke rol in de bouw van klantenprofielen in real time, aangezien twee passende waarden in zelfde namespace twee gegevensbronnen toestaan om een identiteitsgrafiek te vormen.

Beginnen met het maken van een naamruimte voor de [!DNL Luma] loyaliteitsschema:

1. Ga in de gebruikersinterface van het Platform naar **[!UICONTROL Identiteiten]** in de linkernavigatie.

1. Selecteren **[!UICONTROL Naamruimte maken]**.

1. Geef de volgende gegevens op:

   | Weergavenaam | Identiteitssymbool | Type |
   |---|---|---|
   | `Luma Loyalty ID` | `lumaLoyalty` | [!UICONTROL Apparaatoverschrijdende id] |

1. Selecteer **[!UICONTROL Maken]**.

   ![Naamruimten maken](assets/createNamespace.png)

1. Maak nog twee naamruimten na dezelfde stappen:

   | Weergavenaam | Identiteitssymbool | Type |
   |---|---|---|
   | `Luma CRM ID` | `lumaCRM` | [!UICONTROL Apparaatoverschrijdende id] |
   | `Luma Product` | `lumaProduct` | [!UICONTROL Id van niet-personen] |

## Stap 2: Schema&#39;s maken

In deze stap definieert u de structuur van de voorbeeldgegevens door zes [[!UICONTROL schema&#39;s]](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html):

* [[!DNL Luma Loyalty]](#create-luma-loyalty-schema)

* [[!DNL Luma Products]](#create-luma-products-schema)

* [[!DNL Luma Product Inventory Events]](#create-luma-product-inventory-event-schema)

* [[!DNL Luma CRM]](#create-luma-crm-and-luma-product-interactions-schemas)

* [[!DNL Luma Product Interactions]](#create-luma-crm-and-luma-product-interactions-schemas)

* [[!DNL Luma Test Profiles]](#create-luma-crm-and-luma-product-interactions-schemas)

>[!TIP]
>
>Bekijk de videozelfstudie: [Een schema maken](/help/set-up-data/create-schema.md) voordat u begint.

### Maken [!DNL Luma Loyalty] [!UICONTROL Schema] {#create-luma-loyalty-schema}

#### Het schema maken

Begin met het maken van de [!DNL Luma Loyalty] schema:

1. Ga naar **[!UICONTROL GEGEVENSBEHEER]** > **[!UICONTROL Schemas]** in de linkernavigatie.

1. Selecteren **[!UICONTROL Schema maken]** rechtsboven.

1. Selecteer in het vervolgkeuzemenu de optie **[!UICONTROL Afzonderlijk XDM-profiel]**, aangezien u kenmerken van een individuele klant (punten, status, enzovoort) modelleert.

   ![Schema maken](assets/loyaltyCreateSchema.png)

#### Bestaande veldgroepen toevoegen

Vervolgens wordt u gevraagd veldgroepen toe te voegen aan het schema. U moet alle gebieden aan schema&#39;s toevoegen gebruikend groepen. U voegt bestaande veldgroepen toe en moet een veldgroep maken.

>[!NOTE]
>
>Als de [!UICONTROL Veldgroepen] modal wordt niet automatisch geopend op de [!UICONTROL Schemas] pagina, selecteert u **[!UICONTROL Toevoegen]** (zoals weergegeven in de volgende afbeelding).

![Veldgroep toevoegen](assets/add_field_group.png)

1. Op de **[!UICONTROL Veldgroepen toevoegen]** pagina, schakelt u de volgende veldgroepen in:

   * **[!UICONTROL Demografische details]** voor basisgegevens van klanten zoals naam en geboortedatum.

   * **[!UICONTROL Persoonlijke contactgegevens]** voor standaardcontactgegevens zoals e-mailadres en telefoonnummer.

   * **[!UICONTROL Loyalty-details]** voor de loyaliteitsdetails zoals punten, verbonden datum, of status. De groep van het loyaliteitsgebied is ver onderaan de lijst, zodat is het het gemakkelijkst om naar het te zoeken.

1. Selecteren **[!UICONTROL Veldgroep toevoegen]** om alle drie gebiedsgroepen aan het schema toe te voegen.

   ![Standaardveldgroepen selecteren](assets/addstandardFieldGroups.png)

1. Selecteer het bovenste knooppunt van het schema.

1. Enter `Luma Loyalty` als de [!UICONTROL Weergavenaam].

#### Een [!UICONTROL veldgroep]

Om consistentie over de schema&#39;s te verzekeren, adviseert Adobe het beheren van alle systeemherkenningstekens in één enkele groep:

1. Van de **[!UICONTROL Samenstelling]** deel onder [!UICONTROL Veldgroepen], selecteert u **[!UICONTROL Toevoegen]**.

1. Selecteren **[!UICONTROL Nieuwe veldgroep maken]**.

1. Toevoegen `Luma Identifiers` als de **[!UICONTROL Weergavenaam]**.

1. Toevoegen `system identifiers for XDM Individual Profile class` als de **[!UICONTROL Beschrijving]**.

1. Selecteren **[!UICONTROL Veldgroepen toevoegen]**.

   ![Nieuwe veldgroep maken](assets/addnewfieldgroup.png)

#### Velden toevoegen aan de nieuwe [!UICONTROL veldgroep]

De nieuwe, lege veldgroep wordt toegevoegd aan uw schema. Met de knoppen + kunt u nieuwe velden toevoegen aan elke locatie in de hiërarchie. In dit geval moet u velden toevoegen op het hoofdniveau:

1. Selecteren **[!UICONTROL +]** naast de naam van het schema.

   Met deze stap voegt u een veld onder toe **uw huurder** naamruimte, om conflicten te beheren tussen uw aangepaste velden en standaardvelden.

1. In de **[!UICONTROL Veldeigenschappen]** zijbalk voegt u de details van het nieuwe veld toe:

   * **Veldnaam:** `systemIdentifier`

   * **[!UICONTROL Weergavenaam]:** `System Identifier`

   * **Type:** Object

   * **[!UICONTROL Veldgroep toewijzen]:** [!DNL Luma identifiers]

1. Selecteren **[!UICONTROL Toepassen]**.

   ![Systeem-id toevoegen](assets/addsysteidentifier.png)

   Twee velden toevoegen onder de `systemIdentifier` object:

   | [!UICONTROL Veldnaam] | [!UICONTROL Weergavenaam] | [!UICONTROL Type] |
   |-------------|-----------|----------|
   | `loyaltyId` | `Loyalty ID` | [!UICONTROL Tekenreeks] |
   | `crmId` | `CRM Id` | [!UICONTROL Tekenreeks] |

![velden](./assets/add_fields.png)

#### Identiteiten instellen

U hebt nu de naamruimte en de [!DNL Luma] Loyalty-schema geconfigureerd. Voordat u gegevens kunt invoeren, moet u de identiteitsvelden een label geven. Elk schema gebruikt met [!UICONTROL Klantprofiel in realtime] moet een primaire identiteit hebben opgegeven en elke opgenomen record moet een waarde voor dat veld hebben.

1. Stel de **primaire identiteit**:

   Van de `Luma Loyalty` schema:

   1. Selecteer `Luma Identifiers` veldgroep.

   1. Selecteer `loyaltyId` veld.

   1. In de **[!UICONTROL Veldeigenschappen]** de **[!UICONTROL Identiteit]** doos.

   1. De optie **[!UICONTROL Primaire identiteit]** doos.

   1. Selecteer `Luma Loyalty Id` naamruimte van **[!UICONTROL Identiteitsnaamruimten]** vervolgkeuzelijst.

   1. Selecteren **[!UICONTROL Toepassen]**.

      ![primaire identiteit](/help/tutorial-configure-a-training-sandbox/assets/primary_identity.png)

1. Een **secundaire identiteit**:

   Van de `Luma Loyalty` schema:

   1. Selecteer `Luma Identifiers` veldgroep.

   2. Selecteer `crmId` veld.

   3. In de **[!UICONTROL Veldeigenschappen]** de **[!UICONTROL Identiteit]** doos.

   4. Selecteer `Luma CRM Id` naamruimte van **[!UICONTROL Identiteitsnaamruimten]** vervolgkeuzelijst.

   5. Selecteren **[!UICONTROL Toepassen]**.

#### Inschakelen voor profiel en schema opslaan

1. Selecteer het bovenste knooppunt van het schema.

1. In de [!UICONTROL Veldeigenschappen] enable **[!UICONTROL Profiel]**.

   Het schema moet er als volgt uitzien:

   ![Luma-Loyalty-schema](assets/lumaloyaltyschema.png)

1. Selecteren **[!UICONTROL Opslaan]**.

### Maken [!DNL Luma Products] [!UICONTROL Schema] {#create-luma-products-schema}

1. Ga naar [!UICONTROL GEGEVENSBEHEER] -> **[!UICONTROL Schemas]** in de linkernavigatie.

1. Selecteer **[!UICONTROL Schema maken]** aan de rechterbovenzijde.

1. Selecteer in het vervolgkeuzemenu de optie **[!UICONTROL Bladeren door alle schematypen]**, waarmee u een klasse kunt maken.

1. Selecteren **[!UICONTROL Nieuwe klasse maken].

1. Voeg de weergavenaam toe: `Luma Products`.

1. Klasse toewijzen.

1. Een [!UICONTROL veldgroep]:

   * Weergavenaam: `Luma Product Info`

1. Voeg het volgende veld toe aan de [!DNL Luma] [!UICONTROL Product] Informatieveldgroep.

   * Veldnaam: `product`

   * Weergavenaam: `Product`

   * Type: [!UICONTROL Object]

   * Veldgroep: [!DNL Luma Product info]

1. Selecteren **[!UICONTROL Toepassen]**.

1. Voeg de volgende velden toe aan de **[!DNL Product]** object:

   | [!UICONTROL Veldnaam] | [!UICONTROL Weergavenaam] | [!UICONTROL Type] |
   |-------------|-----------|----------|
   | `sku` | `SKU` | [!UICONTROL Tekenreeks] |
   | `name` | `Name` | [!UICONTROL Tekenreeks] |
   | `category` | `Category` | [!UICONTROL Tekenreeks] |
   | `color` | `Color` | [!UICONTROL Tekenreeks] |
   | `size` | `Size` | [!UICONTROL Tekenreeks] |
   | `price` | `Price` | [!UICONTROL Dubbel] |
   | `description` | `Description` | [!UICONTROL Tekenreeks] |
   | `productImageURL` | `Product Image URL` | [!UICONTROL Tekenreeks] |
   | `productURL` | `Product URL` | [!UICONTROL Tekenreeks] |
   | `stockQuantity` | `Stock Quantity` | [!UICONTROL Tekenreeks] |

1. Voeg de **[!UICONTROL Weergavenaam]** `Luma Products` naar het schema.

1. Selecteren **[!UICONTROL Opslaan]**.

### Maken [!DNL Luma Product Inventory Event] [!UICONTROL Schema] {#create-luma-product-inventory-event-schema}

1. Ga naar **[!UICONTROL GEGEVENSBEHEER]** -> **[!UICONTROL Schemas]** in de linkernavigatie.

1. Selecteer **[!UICONTROL Schema maken]** aan de rechterbovenzijde.

1. Selecteer in het vervolgkeuzemenu de optie **[!UICONTROL Bladeren door alle schematypen]**.

1. Selecteren **[!UICONTROL Nieuwe klasse maken]**.

1. Voeg de weergavenaam toe: `Business Event`.

1. Selecteer type: *[!UICONTROL Tijdreeksen]*.

1. Klasse toewijzen.

1. Een [!UICONTROL veldgroep]:

   * Weergavenaam: `Product Inventory Event Details`

1. Voeg de **[!UICONTROL Weergavenaam]** `Luma Product Inventory Event Schema` naar het schema.

1. Voeg het volgende gebied aan de het gebiedsgroep van Info van het Product van de Luma toe:

   * Veldnaam: `inventoryEvent`

   * Weergavenaam: `Inventory Event`

   * Type: [!UICONTROL Object]

   * Veldgroep: [!DNL Product Inventory Event Details]

1. Voeg de volgende velden toe aan de **[!DNL Product Inventory Event Details]** object:

   | [!UICONTROL Veldnaam] | [!UICONTROL Weergavenaam] | [!UICONTROL Type] |
   |-------------|-----------|----------|
   | `productId` | `Product ID` | [!UICONTROL Tekenreeks] |
   | `sku` | `SKU` | [!UICONTROL Tekenreeks] |
   | `stockEventType` | `Stock Event Type` | **[!UICONTROL Enum]** with `restock` en `outOfStock` als waarden |

   1. om de `stockEventType` aan Enum, uitgezochte type: `string`.

   1. Omlaag schuiven naar de onderkant van het dialoogvenster **[!UICONTROL Veldeigenschappen]**.

   1. Inschakelen **[!UICONTROL Enum]**.

   1. Enter **[!UICONTROL waarden] ([!UICONTROL label)]**: `restock` (`restock`).

   1. Selecteren **[!UICONTROL Rij toevoegen]**.

   1. Enter **[!UICONTROL waarden] ([!UICONTROL label)]**: `outOfStock` (`out of stock`).

   1. Selecteren **[!UICONTROL Toepassen]**.

      ![enum](assets/enum.png)

1. Set `productId` veld als **[!UICONTROL primaire identiteit]** gebruiken **[!DNL Luma Product namespace]**.

1. Selecteer `sku` en een relatie met de `product.sku` in het **[!DNL Luma Products]** Schema:

   1. Omlaag schuiven naar de onderkant van het dialoogvenster **[!UICONTROL Veldeigenschappen]**.

   1. Inschakelen **[!UICONTROL Relatie]**.

      1. **[!UICONTROL Referentieschema]**: [!DNL Luma Products].

      1. **[!UICONTROL Naamruimte van verwijzing]**: [!DNL Luma Product].
   1. Selecteren **[!UICONTROL Toepassen]**.

      Het schema moet er als volgt uitzien:

      ![SKU-relatie](assets/sku_relationship.png)


1. Inschakelen voor **Profiel**.

1. Selecteren [!UICONTROL Opslaan] om het schema op te slaan.

### Maak de [!DNL Luma CRM] en [!DNL Luma Product Interactions] schema&#39;s {#create-luma-crm-and-luma-product-interactions-schemas}

Maak de volgende aanvullende [!UICONTROL schema&#39;s]:

| [!UICONTROL Weergavenaam] | [!DNL Luma CRM] | [!DNL Luma Product Interactions] | [!DNL Luma Test Profiles] |
|  ---| ------- | ---- |----|
| **[!UICONTROL Type]** | [!UICONTROL Afzonderlijk XDM-profiel] | [!UICONTROL XDM Experience Event] | [!UICONTROL Afzonderlijk XDM-profiel] |
| **[!UICONTROL Bestaande veldgroep toevoegen]** | Luminantidentificatoren<br>Demografische details<br>Persoonlijke contactgegevens | Identiteitskaart<br>Handelsgegevens | Luminantidentificatoren<br>Demografische details<br>Persoonlijke contactgegevens<br>Details van de profieltest |
| **[!UICONTROL Relatie]** |  | *[!DNL productListItems.SKU]*:<br> Referentieschema *[!DNL Luma Products]* <br>[!DNL Reference identity namespace] *[!DNL Luma Product]* schema |
| **[!UICONTROL Primaire identiteit] [!UICONTROL namespace])** | systemIdentifier.crmId<br>(Luma CRM-id) |  | personalEmail.address<br>(Email) |
| **[!UICONTROL Secundaire identiteit] [!UICONTROL namespace]** | PersonalEmail.address (e-mail)<br>mobilePhone.number (Telefoon) |  |
| **[!UICONTROL Inschakelen voor profiel]** | ja | ja | ja |

## Volgende stappen

Nu u de gegevensstructuur hebt gemaakt, kunt u [gegevenssets maken en voorbeeldgegevens opnemen](/help/tutorial-configure-a-training-sandbox/manual-data-ingestion.md).
