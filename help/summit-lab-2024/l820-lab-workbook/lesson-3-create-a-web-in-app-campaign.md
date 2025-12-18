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
source-git-commit: 55ba1a46c1473d94847e7fccc69ed2a33badb54c
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

1. In Journey Optimizer, in de linkernavigatie, onder **uitgezochte** Campagnes **van het BEHEER van de WEG**.

1. Klik **creeer Campagne**.

   ![ CreateCampaign ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-create-campaign.png)

1. Op **creeer de pagina van de Campagne**, in de **sectie van de Actie**, selecteer het **In-app bericht** controlevakje.

1. Van **verzenden naar** dropdown, uitgezocht **Web.**

1. Ga volgende URL in: **https://dsn.adobe.com/web/adobe-summit-2024/exercise** - *dit is de Web-pagina uw bericht zal verschijnen.*

   ![ In-app URL ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-1-in-app-url.png)

1. Klik **[!UICONTROL creëren]**.

## Oefening 3.2 Uw Campagne vormen

Op deze pagina definieert u de eigenschappen van de campagne en de gebeurtenis die het bericht in de app activeert om op de webpagina te verschijnen. Laat alle andere instellingen op de standaardwaarde staan. Voor deze oefening hoeft u geen specifiek publiek te definiëren.

### 3.2.1 [!UICONTROL  sectie van Eigenschappen ]

1. In de **sectie van Eigenschappen**, geef uw campagne een unieke **Naam**:

   >[!NOTE]
   > Zorg ervoor dat u de naam met het nummer van uw licentie start, zodat u deze eenvoudig kunt gebruiken
   > zoek je campagne later .
   > 
   > Als uw nummer bijvoorbeeld 99 is: 
   >
   > ![ Naam van Eigenschappen ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-properties-name.png)


### 3.2.2 De aangepaste triggerregel instellen

In deze sectie definieert u wat activeert voor het bericht dat op de website wordt weergegeven. U bepaalt een unieke trekker die u toestaat om het bericht enkel naar zich te verzenden.

1. De rol neer aan de **[!UICONTROL sectie van Trekkers]**, dan klikt **[!UICONTROL trekkers]** uitgeeft.

   ![ wijzigt ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. In de regelbouwer, klik op **[!UICONTROL Lancering van de Toepassing]** en van dropdown uitgezochte *Verzonden gegevens aan Platform*.
   ![ drop-down van de trekkergebeurtenis ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Voeg een voorwaarde toe door **[!UICONTROL + te klikken toevoegt voorwaarde]**.

   ![ voeg voorwaardenknoop ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-1-3-add-condition.png) toe

1. Van **[!UICONTROL selecteer een spoor]** daling neer, uitgezochte **[!UICONTROL XDM gebeurtenistype]**.

   ![ XDM gebeurtenistype ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)


1. Op het volgende tekstgebied, voeg a *`<custom string value>`* toe dat u zich kunt herinneren, en druk **** `<custom string value>` toevoegen om de waarde te bewaren.

   Deze aangepaste tekenreekswaarde wordt later gebruikt om uw bericht te verzenden.

   >[!TIP]
   > Door het nummer van uw licentie toe te voegen aan de aangepaste tekenreekswaarde, kunt u deze uniek en gemakkelijker onthouden.
   > 
   > Bijvoorbeeld: `99web`
   > 

   ![ voeg de waarde van het douanetrekkerkoord van de douanetrekker ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-add-custom-trigger-dropdown.png) toe

1. Druk de **[!UICONTROL Gereed]** knoop in het hoogste recht.

>[!SUCCESS]
>
>U hebt nu uw web in-app bericht gedefinieerd met een aangepaste trigger-gebeurtenis.
>
>![ campagne van het Web met gedefiniëerde douanetrekker ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-2-web-campaign-with-custom-trigger.png)


### 3.2.3 De inhoud van het bericht in de app bewerken

In deze sectie definieert u de inhoud, het ontwerp en de lay-out van uw bericht.

1. Klik **uitgeven inhoud** knoop in de **sectie van de Actie** om tot de auteursconstructie toegang te hebben.

   ![ geef inhoudknoop ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png) uit

1. Het ontwerpproces is hetzelfde proces als dat u hebt uitgevoerd in de bovenstaande oefeningen voor mobiele in-app. Neem de tijd om uw bericht vrij te bewerken met uw eigen titel, tekst en media-inhoud.

   Als u de modale lay-out of de lay-out Volledig scherm gebruikt, kunt u een knop toevoegen. U kunt dit URL gebruiken om de productpagina te openen: **https://dsn.adobe.com/web/adobe-summit-2024/P2WsaDPf_**

1. Wanneer u klaar bent met het uitgeven van uw bericht, klik **[!UICONTROL Overzicht om]** te activeren.

1. Als alles goed op het overzichtsscherm kijkt, activeert de klik **** om uw Web in-app bericht te publiceren.

1. U wordt teruggestuurd naar het campagnedashboard.

   Wacht eenheid uw veranderingen van de campagnestatus in **Levend** alvorens zich aan 4.1.4 te bewegen.

## Oefening 3.3 Het web in-app-bericht activeren

1. Ga naar de website Fréscopa en navigeer aan de **Uitoefening** pagina op uw browser.

   ![ de oefeningen van het Web verbinding ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-2-frescopa-web-exercise-link.png)

1. Vernieuw de webpagina.

1. Typ de unieke tekenreekswaarde die u in de campagne hebt gedefinieerd.

   ![ uitoefeningspagina ](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-2-exercise-page.png)

1. Klik **[!UICONTROL verzenden]**.

>[!SUCCESS]
>
>Als u op de knop Verzenden klikt met uw unieke waarde, wordt het bericht Web In-app geactiveerd. En u zou uw Web in-app bericht op uw scherm moeten zien verschijnen.
>
>Deze oefening simuleerde een douane XDM verzendt gebeurtenis die u door uw Fréscopa klantenervaring zag.


## Aanvullende bronnen

**hoe te video&#39;s:**

* [Een in-app-campagne maken](/help/channels/create-an-in-app-campaign.md)
* [Een in-app bericht schrijven](/help/channels/author-in-app-messages.md)

**documentatie van het Product:**

* [ worden begonnen met in-app kanaal ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/get-started-in-app)
* [ creeer een Web in-app bericht ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/create-in-app-web)
* [ Ontwerp uw inhoud in-app ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/design-in-app)
* [ Controle en verzend uw bericht In-app ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/in-app/send-in-app)
