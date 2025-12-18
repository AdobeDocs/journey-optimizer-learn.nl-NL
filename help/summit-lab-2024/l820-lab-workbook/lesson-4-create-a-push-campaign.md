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
source-git-commit: 55ba1a46c1473d94847e7fccc69ed2a33badb54c
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

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

1. In Journey Optimizer, in de linkernavigatie, in de **[!UICONTROL sectie van het BEHEER van de 1&rbrace; JOURNEY, uitgezochte]** Campagnes **.**

1. Klik **[!UICONTROL creeer Campagne]**.

   ![&#x200B; creeer Campagne &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Op **[!UICONTROL creeer de pagina van de Campagne]**, in de **[!UICONTROL sectie van de Actie]**, selecteer het **[!UICONTROL Push bericht]** controlevakje.

1. Van het **[!UICONTROL oppervlak van de App]** dropdown, uitgezochte *[!DNL Frecopa-Push]*.

1. Klik **[!UICONTROL creeer]** om een drukkampagne tot stand te brengen.

   ![&#x200B; oppervlakte van de Toepassing &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-2-app-surface.png)

>[!SUCCESS]
>
>U moet nu op de pagina Campagneeigenschappen staan:
> ![Campagneeigenschappen &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-2-campaign-properties.png)

## Oefening 4.2 - Uw campagne configureren

Op deze pagina, vormt u de eigenschappen, het publiek, de acties, en het programma van uw campagne.

### 4.2.1 [!UICONTROL &#x200B; sectie van Eigenschappen &#x200B;]

Geef uw campagne een naam. Zorg ervoor dat u de naam met het nummer van uw licentie start, zodat u de campagne eenvoudig kunt vinden wanneer u ernaar zoekt.

Als uw nummer van de licentie bijvoorbeeld 99 is: `99 - 10% Discount Campaign` .

### 4.2.2 **[!UICONTROL sectie van het publiek]**

1. In de publiekssectie, klik **[!UICONTROL Uitgezochte publiek]**.

   ![&#x200B; publiekssectie &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-2-5-audience-section.png)

1. Op het **[!UICONTROL Uitgezochte publiek]** scherm, onderzoek naar het publiek:

   **Laboratorium - Plaats`your seat number`**

1. Selecteer het publiek, dan klik **[!UICONTROL sparen]**.

   ![&#x200B; publieksselectie &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-2-7-select-audience.png)

### 4.2.3 De inhoud van de pushmelding bewerken

In deze oefening, ontwerpt u en past u de pushmelding aan.

1. In de **[!UICONTROL sectie van de Actie]**, klik **[!UICONTROL uitgeven Inhoud &#x200B;] knoop**.

   ![&#x200B; geef inhoudknoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-action-edit-content-button.png) uit

1. Op het volgende scherm selecteert u, afhankelijk van het mobiele apparaat dat u hebt, het tabblad [!DNL iOS™] of [!DNL Android™] om de inhoud te configureren.

>[!BEGINTABS]

>[!TAB  iOS ]

![&#x200B; iOS tabel &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-ios-tab.png)

>[!TAB  Android ]

![&#x200B; Android tabel &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-android-tab.png)

>[!ENDTABS]

#### 4.2.3.1 [!UICONTROL &#x200B; stel de sectie van het Bericht &#x200B;] samen

1. **stel uw bericht samen:** voel vrij om het even welke tekst toe te voegen u zou willen. Hier volgen enkele voorbeelden die u kunt gebruiken:

   * Titel: `Get 10% off today!`
   * Platte tekst: `Today only! Get 10% off on your House Blend coffee purchase!`

     ![&#x200B; stel bericht &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-compose-message.png) samen

#### 4.2.3.2 Verandering op klikgedrag van het bericht om **een productpagina** te openen

1. In **[!UICONTROL op klikgedrag]** sectie, uitgezochte **[!UICONTROL Deeplink]** van het **[!UICONTROL Lichaam klikt gedrag]** dropdown.

1. Kopieer en kleef volgende URL in het **gebied URL**:

   `dxdemo://exoticVibes`

   ![&#x200B; diepe verbinding &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-deeplink.png)

#### 4.2.3.3 Een afbeelding toevoegen aan het bericht

1. In **[!UICONTROL voeg media]** sectie toe, klik **[!UICONTROL media]** toevoegen.

   ![&#x200B; voeg media knopen &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-3-add-media-buttons.png) toe

1. Op het **[!UICONTROL Uitgezochte scherm van Assets]**, in de linkernavigatie, open de **omslag Fréscopa** en selecteer een beeld van die omslag.

   Bijvoorbeeld: `HouseBlend.png`

1. Klik het beeld en klik **[!UICONTROL Uitgezochte &#x200B;] knoop** om het beeld aan uw duw bericht toe te voegen.

   ![&#x200B; uitgezochte beeld &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-3-select-image.png)

   >[!SUCCESS]
   >
   > 1. Voor het voorproefscherm, klik **[!UICONTROL uitbreiden Mening]**.
   > 1. Geef een voorvertoning van uw bericht weer.
   > <br>
   >
   > ![&#x200B; breid mening &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-expand-view.png) uit

### Bonus Exercise

Als u dit gedeelte van de oefening hebt voltooid en nog tijd hebt, probeert u de bonusoefening:

+++ Bonusoefening

#### Personaliseer het bericht dat u verzendt door de voornaam van de ontvanger toe te voegen

1. Klik **verpersoonlijkingsdialoog** naast het **[!UICONTROL gebied van het Lichaam]**.

   ![&#x200B; verpersoonlijkingsknoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalization-button.png)

1. Voor het **verpersoonlijkingsdialoog** scherm, plaats de curseur waar u de voornaam in de tekst wilt toevoegen.

1. Zorg ervoor dat de **attributen van het Profiel** in de linkernavigatie worden geselecteerd.

   ![&#x200B; attribuut van het Profiel &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalize-body-profile-attributes.png)

1. Op het **gebied van het Onderzoek**, onderzoek naar: `first name`.

1. Klik **+** naast **Voornaam (de attributen van het Profiel>Persoon>Volledige naam)** om het verpersoonlijkingsgebied aan uw tekst toe te voegen.

   ![&#x200B; Onderzoek naar voornaam &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalize-search-first-name.png)

   >[!SUCCESS]
   >
   > Zo ziet uw tekst eruit:
   > 
   >![&#x200B; het teken van Personalization &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-personalization-token.png)

1. Klik **[!UICONTROL sparen]** om de verpersoonlijking te bewaren.


   >[!SUCCESS]
   >
   > 1. Voor het voorproefscherm, klik **[!UICONTROL uitbreiden Mening]**.
   > 1. Geef een voorvertoning van uw bericht weer.
   > 
   > ![&#x200B; breid mening &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-3-expand-view.png) uit

+++

### 4.2.4. Reviseren en activeren

Als je tevreden bent met de inhoud van je bericht, kun je het bericht activeren:

1. Klik **[!UICONTROL Overzicht om]** te activeren.

   ![&#x200B; overzicht en activeer knoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-4-review-and-activate-button.png)

1. Op het **[!UICONTROL Overzicht om]** scherm te activeren, klik **[!UICONTROL activeert]**.

   ![&#x200B; overzicht om het scherm &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-4-review-to-activate.png) te activeren

>[!SUCCESS]
> Voor de **pagina van het overzicht van Campagnes**, vind uw campagne en controleer de status.
>
> ![&#x200B; campagnestatus &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-push-completed.png)
> 
> De status verandert van verwerking naar live, naar voltooid - dit kan een paar minuten duren.
> Nadat de status is gewijzigd in voltooid:
>
> ![&#x200B; duw resultaten &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-push-notification-result.png)

## Aanvullende bronnen

**hoe te video&#39;s:**

* [Een pushcampagne configureren en verzenden](/help/channels/create-a-push-campaign.md)

**documentatie van het Product:**

* [&#x200B; worden begonnen met duw bericht &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/push/get-started-push)
* [Een pushmelding maken](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/push/create-push)
* [&#x200B; Ontwerp een duw- bericht &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/push/design-push)
* [&#x200B; Controle en verzend uw pushbericht &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/push/send-push)
