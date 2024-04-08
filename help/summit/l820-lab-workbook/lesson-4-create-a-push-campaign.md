---
title: Les 4 - Een pushcampagne maken
description: Bekijk de profielgegevens en leer hoe u een pushmelding maakt en verstuurt naar het publiek in Journey Optimizer.
feature: Push
role: User
level: Intermediate
doc-type: Tutorial
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14980
exl-id: 0f82d6a5-18c0-45f2-968e-a678fc2d5768
source-git-commit: befde57252ebc12c5d6df31fde8078e4535d1261
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 1%

---

# Les 4 - Een pushcampagne maken

In de vorige exercitie was je een koffieliefhebber, een Fréscopa-klant. U communiceerde met het merk via hun website en de Fréscopa-app en ontving veel transactieberichten. Deze berichten worden geactiveerd door de interactie van de gebruiker met de website of de toepassing.

In deze exercitie, zult u uw markeringspost op zetten en een marketing campagne voor Frésopa uitvoeren, die het drukkende kanaal zal gebruiken om de gebruikers van de Fréscopa app te richten. Met pushberichten worden gebruikers van de app op de hoogte gehouden, zelfs als ze de app niet gebruiken, maar ook om ze weer te laten deelnemen aan de app. Het doel is de klant te stimuleren om het huismengsel te kopen door een korting van 10% aan te bieden.

## Leerdoelen

* Weet hoe u een pushcampagne kunt maken.
* Begrijp hoe u een pushbericht ontwerpt.

<br>

## Oefening 4.1 - Een pushcampagne maken

In deze oefening, creeert u de pushcampagne, ontwerp, en past de dupmelding aan, en verzendt het dupbericht naar uw eigen apparaat.

1. In Journey Optimizer, in de linkernavigatie, in **[!UICONTROL JOURNEYBEHEER]** sectie, selecteert u **Campagnes**.

1. Klikken **[!UICONTROL Campagne maken]**.

   ![Campagne maken](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Op de **[!UICONTROL Campagne maken]** pagina, in de  **[!UICONTROL Handeling]** selecteert u de **[!UICONTROL Pushmelding]** selectievakje.

1. Van de **[!UICONTROL App-oppervlak]** vervolgkeuzelijst, selecteren *[!DNL Frecopa-Push]*.

1. Klikken **[!UICONTROL Maken]** om een pushcampagne te maken.

   ![App-oppervlak](/help/summit/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>U moet nu op de pagina Campagneeigenschappen staan:
> ![Campagneigenschappen](/help/summit/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## Oefening 4.2 - Uw campagne configureren

Op deze pagina, vormt u de eigenschappen, het publiek, de acties, en het programma van uw campagne.

### 4.2.1. [!UICONTROL Sectie Eigenschappen]

Geef uw campagne een naam. Zorg ervoor dat u de naam met het nummer van uw licentie start, zodat u de campagne eenvoudig kunt vinden wanneer u ernaar zoekt.

Als uw nummer bijvoorbeeld 99 is: `99 - 10% Discount Campaign`.

### 4.2.2. **[!UICONTROL Sectie Publiek]**

1. Klik in de sectie voor het publiek op **[!UICONTROL Doelgroep selecteren]**.

   ![doelsectie](/help/summit/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. Op de **[!UICONTROL Doelgroep selecteren]** scherm, zoekopdracht naar publiek:

   **Lab - Zitplaats`your seat number`**

1. Selecteer het publiek en klik op **[!UICONTROL Opslaan]**.

   ![doelselectie](/help/summit/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3 De inhoud van de pushmelding bewerken

In deze oefening, ontwerpt u en past u de pushmelding aan.

1. In de **[!UICONTROL Handeling]** klikt u op de **[!UICONTROL Inhoud bewerken] knop**.

   ![Knop Inhoud bewerken](/help/summit/l820-lab-workbook/assets/2-3-action-edit-content-button.png)

1. Selecteer in het volgende scherm, afhankelijk van het mobiele apparaat dat u hebt, de optie [!DNL iOS™] of [!DNL Android™] om uw inhoud te configureren.

>[!BEGINTABS]

>[!TAB iOS]

![Het tabblad iOS](/help/summit/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB Android]

![Tabblad Android](/help/summit/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1 [!UICONTROL Bericht samenstellen] sectie

1. **Stel uw bericht samen:** Voel u vrij om tekst toe te voegen die u wilt. Hier volgen enkele voorbeelden die u kunt gebruiken:

   * Titel: `Get 10% off today!`
   * Platte tekst: `Today only! Get 10% off on your House Blend coffee purchase!`

     ![Bericht samenstellen](/help/summit/l820-lab-workbook/assets/2-3-compose-message.png)

#### 4.2.3.2 Het gedrag van het bericht bij klikken wijzigen in **een productpagina openen**

1. In de **[!UICONTROL Bij klikken, gedrag]** sectie, selecteert u **[!UICONTROL Deeplink]** van de **[!UICONTROL Klikgedrag hoofdtekst]** vervolgkeuzelijst.

1. Kopieer en plak de volgende URL in de **URL-veld**:

   `dxdemo://exoticVibes`

   ![diepe koppeling](/help/summit/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3 Een afbeelding aan het bericht toevoegen

1. In de **[!UICONTROL Media toevoegen]** sectie, klikken **[!UICONTROL Media toevoegen]**.

   ![Media toevoegen, knoppen](/help/summit/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png)

1. Op de **[!UICONTROL Elementen selecteren]** het scherm, in de linkernavigatie, open **Map Fréscopa** en selecteer een afbeelding uit die map.

   Bijvoorbeeld: `HouseBlend.png`

1. Klik op de afbeelding en klik op de knop **[!UICONTROL Selecteren] knop** om de afbeelding aan uw pushmelding toe te voegen.

   ![afbeelding selecteren](/help/summit/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. Klik in het voorvertoningsscherm op **[!UICONTROL Weergave uitbreiden]**.
   > 1. Geef een voorvertoning van uw bericht weer.
   > <br>
   >
   > ![weergave uitbreiden](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

### Bonus Exercise

Als u dit gedeelte van de oefening hebt voltooid en nog tijd hebt, probeert u de bonusoefening:

+++ Bonusoefening

#### Personaliseer het bericht dat u verzendt door de voornaam van de ontvanger toe te voegen

1. Klikken **verpersoonlijkingsdialoog** naast de **[!UICONTROL Lichaam]** veld.

   ![personalisatieknop](/help/summit/l820-lab-workbook/assets/2-3-personalization-button.png)

1. Op de **verpersoonlijkingsdialoog** -scherm, plaatst u de cursor op de plaats waar u de voornaam wilt toevoegen aan de tekst.

1. Zorg ervoor dat de **Profielkenmerken** worden geselecteerd in de linkernavigatie.

   ![Profielattribuut](/help/summit/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. In de **Zoekveld**, zoeken naar: `first name`.

1. Klikken **+** naast de **Voornaam (profielkenmerken>Persoon>Volledige naam)** om het verpersoonlijkingsgebied aan uw tekst toe te voegen.

   ![Voornaam zoeken](/help/summit/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > Zo ziet uw tekst eruit:
   > 
   >![Token voor personalisatie](/help/summit/l820-lab-workbook/assets/2-3-personalization-token.png)

1. Klikken **[!UICONTROL Opslaan]** om de personalisatie op te slaan.


   >[!SUCCESS]
   >
   > 1. Klik in het voorvertoningsscherm op **[!UICONTROL Weergave uitbreiden]**.
   > 1. Geef een voorvertoning van uw bericht weer.
   > 
   > ![weergave uitbreiden](/help/summit/l820-lab-workbook/assets/2-3-3-expand-view.png)

+++

### 4.2.4. Reviseren en activeren

Als je tevreden bent met de inhoud van je bericht, kun je het bericht activeren:

1. Klikken **[!UICONTROL Controleren om te activeren]**.

   ![de knop Reviseren en activeren](/help/summit/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. Op de **[!UICONTROL Controleren om te activeren]** scherm, klikken **[!UICONTROL Activeren]**.

   ![revisie om scherm te activeren](/help/summit/l820-lab-workbook/assets/2-3-4-review-to-activate.png)

>[!SUCCESS]
> Op de **Pagina met overzicht van campagnes**, zoek je campagne en controleer de status.
>
> ![campagnestatus](/help/summit/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> De status verandert van verwerking naar live, naar voltooid - dit kan een paar minuten duren.
> Nadat de status is gewijzigd in voltooid:
>
> ![push-resultaten](/help/summit/l820-lab-workbook/assets/2-3-push-notification-result.png)

## Aanvullende bronnen

**Hoe kan ik-video&#39;s:**

* [Een pushcampagne configureren en verzenden](/help/channels/create-a-push-campaign.md)

**Productdocumentatie:**

* [Aan de slag met pushmeldingen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/get-started-push)
* [Een pushmelding maken](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/create-push)
* [Een pushmelding ontwerpen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/design-push)
* [Controleer en verzend uw pushmelding](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/push/send-push)
