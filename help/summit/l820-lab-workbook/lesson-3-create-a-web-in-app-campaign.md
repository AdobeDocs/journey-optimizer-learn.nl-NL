---
title: Les 3 - Een webcampagne in de app maken
description: Maak en activeer een webcampagne in de app.
feature: In App
role: User
level: Intermediate
doc-type: Article
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-13983
thumbnail: KT-13983.jpeg
exl-id: 0f84adfb-edb1-47fa-b696-58eec2b33bb1
source-git-commit: 4f5c92f79eba3651b3633b7850e993160cb1f72c
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# Les 3 - Een in-app campagne voor het web maken

Nu u mobiele ervaringen voor de app hebt gemaakt, maakt u in deze les een van de ervaringen die u op de Fréscopa-website hebt gezien. U maakt een webcampagne in de app. U ontwerpt en past een bericht aan en definieert een trigger die het bericht activeert.

## Leerdoelstellingen

* In-app campagne maken.
* Trigger een bericht in de app.

## Oefening 3.1 Een webcampagne in de app maken

In deze oefening creeert u de campagne en bepaalt welke Web-pagina het in-app bericht verschijnt op.

1. In Journey Optimizer, in de linkernavigatie, onder **JOURNEYBEHEER** selecteren **Campagnes**.

1. Klikken **Campagne maken**.

   ![CreateCampaign](/help/summit/l820-lab-workbook/assets/4-1-create-campaign.png)

1. Op de **Campagne maken** pagina, in de **Handeling** selecteert u de **Bericht in de app** selectievakje.

1. Van de **Verzenden naar** vervolgkeuzelijst, selecteren **Web.**

1. Voer de volgende URL in: **https://dsn.adobe.com/web/adobe-summit-2024/exercise** - *Dit is de webpagina waarop uw bericht wordt weergegeven.*

   ![In-app-URL](/help/summit/l820-lab-workbook/assets/4-1-1-in-app-url.png)

1. Klikken **[!UICONTROL Maken]**.

## Oefening 3.2 Uw Campagne vormen

Op deze pagina definieert u de eigenschappen van de campagne en de gebeurtenis die het bericht in de app activeert om op de webpagina te verschijnen. Laat alle andere instellingen op de standaardwaarde staan. Voor deze oefening hoeft u geen specifiek publiek te definiëren.

### 3.2.1. [!UICONTROL Sectie Eigenschappen]

1. In de **Eigenschappen** deel, geef uw campagne een unieke **Naam**:

   >[!NOTE]
   > Zorg ervoor dat u de naam met het nummer van uw licentie start, zodat u deze eenvoudig kunt gebruiken
   > zoek je campagne later .
   > 
   > Als uw nummer bijvoorbeeld 99 is: 
   >
   > ![Naam eigenschappen](/help/summit/l820-lab-workbook/assets/4-1-2-properties-name.png)


### 3.2.2 De aangepaste triggerregel instellen

In deze sectie definieert u wat activeert voor het bericht dat op de website wordt weergegeven. U bepaalt een unieke trekker die u toestaat om het bericht enkel naar zich te verzenden.

1. Omlaag schuiven naar de **[!UICONTROL Sectie Triggers]** en klik vervolgens op **[!UICONTROL Triggers bewerken]**.

   ![wijzigen](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klik in de regelbouwer op **[!UICONTROL Toepassing starten]** en vanuit de vervolgkeuzelijst selecteert u  *Gegevens verzonden naar platform*.
   ![drop-down gebeurtenis activeren](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Voeg een voorwaarde toe door te klikken **[!UICONTROL + Voorwaarde toevoegen]**.

   ![knop voor toevoegen aan voorwaarde](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Van de **[!UICONTROL Een kenmerk selecteren]** vervolgkeuzelijst, selecteren **[!UICONTROL XDM-gebeurtenistype]**.

   ![XDM-gebeurtenistype](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)


1. Voeg in het volgende tekstveld een *`<custom string value>`* dat u zich kunt herinneren, en drukken **[!UICONTROL Toevoegen]** `<custom string value>` om de waarde op te slaan.

   Deze aangepaste tekenreekswaarde wordt later gebruikt om uw bericht te verzenden.

   >[!TIP]
   > Door het nummer van uw licentie toe te voegen aan de aangepaste tekenreekswaarde, kunt u deze uniek en gemakkelijker onthouden.
   > 
   > Bijvoorbeeld: `99web`
   > 

   ![aangepaste tekenreekswaarde voor trigger toevoegen](/help/summit/l820-lab-workbook/assets/4-1-2-add-custom-trigger-dropdown.png)

1. Druk op **[!UICONTROL Gereed]** rechtsboven.

>[!SUCCESS]
>
>U hebt nu uw web in-app bericht gedefinieerd met een aangepaste trigger-gebeurtenis.
>
>![Webcampagne met aangepaste trigger gedefinieerd](/help/summit/l820-lab-workbook/assets/4-1-2-2-web-campaign-with-custom-trigger.png)


### 3.2.3 De inhoud van het bericht in de app bewerken

In deze sectie definieert u de inhoud, het ontwerp en de lay-out van uw bericht.

1. Klik op de knop **Inhoud bewerken** in de **Handeling** voor toegang tot het ontwerpconstruct.

   ![Knop Inhoud bewerken](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

1. Het ontwerpproces is hetzelfde proces als dat u hebt uitgevoerd in de bovenstaande oefeningen voor mobiele in-app. Neem de tijd om uw bericht vrij te bewerken met uw eigen titel, tekst en media-inhoud.

   Als u de modale lay-out of de lay-out Volledig scherm gebruikt, kunt u een knop toevoegen. U kunt deze URL gebruiken om de productpagina te openen: **https://dsn.adobe.com/web/adobe-summit-2024/P2WsaDPf_**

1. Als u klaar bent met het bewerken van uw bericht, klikt u op **[!UICONTROL Controleren om te activeren]**.

1. Als alles er goed uitziet op het revisiescherm, klikt u op **[!UICONTROL Activeren]** om uw Web in-app bericht te publiceren.

1. U wordt teruggestuurd naar het campagnedashboard.

   Uw wijzigingen in de campagestatus wachten op **Live** vóór de overgang naar punt 4.1.4.

## Oefening 3.3 Het web in-app-bericht activeren

1. Ga naar de Fréscopa-website en ga naar de **Uitoefening** pagina in uw browser.

   ![Weefoefeningen-koppeling](/help/summit/l820-lab-workbook/assets/4-2-frescopa-web-exercise-link.png)

1. Vernieuw de webpagina.

1. Typ de unieke tekenreekswaarde die u in de campagne hebt gedefinieerd.

   ![uitoefenpagina](/help/summit/l820-lab-workbook/assets/4-2-exercise-page.png)

1. Klikken **[!UICONTROL Verzenden]**.

>[!SUCCESS]
>
>Als u op de knop Verzenden klikt met uw unieke waarde, wordt het bericht Web In-app geactiveerd. En u zou uw Web in-app bericht op uw scherm moeten zien verschijnen.
>
>Deze oefening simuleerde een douane XDM verzendt gebeurtenis die u door uw Fréscopa klantenervaring zag.


## Aanvullende bronnen

**Hoe kan ik-video&#39;s:**

* [Een in-app-campagne maken](/help/channels/create-an-in-app-campaign.md)
* [Een in-app bericht schrijven](/help/channels/author-in-app-messages.md)

**Productdocumentatie:**

* [Aan de slag met In-app-kanaal](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [Een Web In-app-bericht maken](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app-web)
* [In-app-inhoud ontwerpen](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [In-app-meldingen controleren en verzenden](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
