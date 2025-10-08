---
title: Les 2 - Een mobiele campagne in de app maken
description: Maak een mobiele in-app-campagne en activeer deze.
feature: In App
role: User
level: Intermediate
doc-type: Article
duration: 0
recommendations: noDisplay, noCatalog
jira: KT-14983
thumbnail: KT-14983.jpeg
exl-id: fe18eca7-229c-4867-ab34-1862bad63124
source-git-commit: 201470e35095b38617d1a1bb5d7b16c1e60f431e
workflow-type: tm+mt
source-wordcount: '1432'
ht-degree: 0%

---

# Les 2 - Een mobiele campagne in de app maken

In deze les maakt en activeert u mobiele berichten in de app.

## Leerdoelen

* Begrijp hoe in-app berichten worden teweeggebracht.
* Leer hoe u een campagne voor mobiele apparaten in de app maakt.
* Trigger een bericht in de app.

## Oefening 2.1 - Aanmelden bij Journey Optimizer

1. Open [&#x200B; Adobe Journey Optimizer &#x200B;](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
2. Meld u aan met de volgende gegevens:
   <br>
   **Gebruikersnaam:** L820+**`<your seat number>`**@adobeeventlab.com
   **Wachtwoord:**   Adobe2024!
   <br>
U kunt de details voor uw login op uw bureaublad van de laboratoriummachine vinden. Gebruik de Adobe ID en het Wachtwoord.
   ![&#x200B; Desktop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/desk-top.png)

   ![&#x200B; Login scherm &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-1-1-ajo-sign-in.png)
   <br>
3. U kunt de volgende twee schermen overslaan:
   <br>
   ![&#x200B; Aantal van de Telefoon &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-1-3-ajo-add-phone.png)
   <br>
   ![&#x200B; pop-up van Personalization &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>U moet zich aanmelden bij Journey Optimizer en op de startpagina:
>
>![&#x200B; Homepage van AJO &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)


## Oefening 2.2 Een mobiele campagne in de app maken

In deze oefening, creeert u een binnen-app overseinencampagne, die wordt teweeggebracht, wanneer u app opent.

1. In Journey Optimizer, in de linkernavigatie, uitgezochte **[!UICONTROL Campagnes]**.

1. Klik **[!UICONTROL creeer Campagne]**.

   ![&#x200B; creeer Campagne &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Op **[!UICONTROL creeer de pagina van de Campagne]**, in de **[!UICONTROL sectie van de Actie]**, selecteer het **[!UICONTROL In-app bericht]** controlevakje.

1. Van **[!UICONTROL verzend naar]** dropdown, uitgezochte **[!DNL Mobile]**.

1. Van het **[!UICONTROL oppervlak van de App]** dropdown, uitgezochte **[!DNL Frecopa Mobile App]**.

1. Klik **[!UICONTROL creëren]**.

   ![&#x200B; oppervlakte van de Toepassing &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-1-1-create.png)

>[!SUCCESS]
>
>U moet nu op de eigenschappen van de Campagne staan:
>
> ![&#x200B; eigenschappen van de Campagne &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-1-2-campaign-properties.png)

## Oefening 2.3 Uw campagne configureren

### 2.3.1 [!UICONTROL &#x200B; sectie van Eigenschappen &#x200B;]

Geef uw campagne een naam. Zorg ervoor dat u de naam met het nummer van uw licentie start, zodat u de campagne eenvoudig opnieuw kunt vinden.

Als uw nummer van de licentie bijvoorbeeld 99 is: `99 - Welcome Campaign` .

![&#x200B; eigenschappen sectie &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-2-1-properties-section.png)

### 2.3.2 De aangepaste triggerregel instellen

1. De rol neer aan de **[!UICONTROL sectie van Trekkers]**, dan klikt **[!UICONTROL trekkers]** uitgeeft.

   ![&#x200B; wijzigt &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. In de regelbouwer, klik op **[!UICONTROL Lancering van de Toepassing]** en van dropdown uitgezochte *Verzonden gegevens aan Platform*.
   ![&#x200B; Verzonden naar gegevensplatform &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Voeg een voorwaarde toe door **[!UICONTROL te klikken toevoegt voorwaarde]**.

   ![&#x200B; voeg voorwaardenknoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-1-3-add-condition.png) toe

1. Van **[!UICONTROL selecteer een spoor]** daling neer, uitgezochte **[!UICONTROL XDM gebeurtenistype]**.

   ![&#x200B; XDM gebeurtenistype &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)

1. Voeg in het volgende tekstveld een *`<custom string value>`* toe die u kunt onthouden.

1. Om de waarde te bewaren, klik ** [!UICONTROL &#x200B; toevoegen* &#x200B;] `<custom string value>`.

   Deze aangepaste tekenreekswaarde wordt later gebruikt om uw bericht te verzenden.

   >[!TIP]
   > Door het nummer van uw licentie toe te voegen aan de aangepaste tekenreekswaarde, kunt u deze uniek en gemakkelijker onthouden.
   > 
   > Bijvoorbeeld: `99exerciseTrigger`

   ![&#x200B; voeg de waarde van het douanetrekkerkoord van de douanetrekker &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-2-2-add-custom-trigger.png) toe

1. Klik **[!UICONTROL Gedaan]** in het hoogste recht.

>[!SUCCESS]
>
>U hebt nu uw bericht in de app gedefinieerd met een aangepaste triggergebeurtenis.
>
>![&#x200B; Campagne met gedefiniëerde douanetrekker &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-2-2-campaign-with-custom-trigger.png)


### 2.3.3 De inhoud van het bericht in de app bewerken

In de **[!UICONTROL sectie van de Actie]**, klik **[!UICONTROL geef Inhoud]** uit.

![&#x200B; geef inhoudknoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png) uit

De [!UICONTROL &#x200B; redacteursvertoningen van het bericht in-app van 0&rbrace; &lbrace;, waar u de inhoud van het in-app bericht vormt.]

#### 2.3.3.1 Layout

Selecteer welke lay-out op uw bericht zou moeten worden toegepast.

Bijvoorbeeld, klik **[!UICONTROL Modal]** om uw in-app bericht een modale lay-out te maken.

![&#x200B; modale knoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-modal-button.png)

#### 2.3.3.2 Uw bericht ontwerpen en uw campagne publiceren

1. Plak in de sectie Media in de volgende URL: `https://t3.ftcdn.net/jpg/02/79/42/52/240_F_279425217_Hr9VBkknMr4fTpuZbxZXfcYdC7jSvGl2.jpg`
   <br>
Wanneer u buiten het waardeveld klikt, wordt de afbeelding weergegeven.

   ![&#x200B; media die op de voorproef &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-media.png) worden getoond

2. In de volgende **[!UICONTROL sectie van de Inhoud]**, voeg in uw eigen douanetekst toe die u in uw bericht voor de **[!UICONTROL Kopbal]** en **[!UICONTROL Lichaam]** wilt worden getoond.

   ![&#x200B; Kopbal en Lichaam &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-content.png)

3. Aanvullende opties:
   1. **Knopen:**

      ![&#x200B; sectie van Knopen &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-buttons.png)

      1. In dit gedeelte van de editor kunt u de tekst voor de CTA-knop aanpassen door het veld Knoptekst te bewerken.

      2. Het **[!UICONTROL Interactieve gebeurtenisgebied]** wordt gebruikt om de waarde te bepalen die tot SDK wordt overgegaan wanneer CTA door de gebruiker wordt gedrukt.

      3. Het **[!UICONTROL gebied van het Doel]** wordt gebruikt om te bepalen waar u CTA zou willen om de gebruiker te nemen. Dit omvat URLs en Deplinks. U kunt deze koppeling bijvoorbeeld toevoegen aan een productpagina zoals `dxdemo://exoticVibes` .

      4. U kunt extra knoppen toevoegen door op de knop **[!UICONTROL + Toevoegen]** te drukken.

      5. Wanneer een tweede knoop aan uw bericht wordt toegevoegd, hebt u nu de optie om de knooplay-out met de drop-down doos te veranderen.


   2. **Geavanceerde het formatteren**

      ![&#x200B; geavanceerd het formatteren knevel &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-toggle.png)

      Als u deze schakeloptie inschakelt, krijgt u extra aanpassingsopties in de editor.

      1. Mediaformaat
      1. Lettertype
      1. Pt-grootte
      1. Lettertypekleur
      1. Uitlijning

      ![&#x200B; geavanceerde het formatteren opties &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-options.png)

   3. **het Lusje van Montages**

      Door over te schakelen naar dit lusje en in de **[!UICONTROL sectie van de Voorproef]**, kunt u de **Voorproef van de App** veranderen.
      <br>\
      ![&#x200B; het lusje van Montages &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-1-settings-tab.png)
      <br>

      1. De **[!UICONTROL sectie van de Lay-out]** geeft u optie om een beeld als achtergrond of een stevige kleur te gebruiken.

      2. De **[!UICONTROL sectie van het Bericht]** verstrekt douaneinteractie die voor uw bericht kan worden toegelaten:
         1. Aangepaste bewegingen
         2. UI-overname
         3. Aangepaste UI-overname
         4. Aangepaste grootte
         5. Aangepaste positie
         6. Aangepaste animatie
         7. Hoek voor bericht
   <br>
4. Wanneer u wordt gedaan creërend uw inhoud en met u bericht tevreden bent klikt het **[!UICONTROL Overzicht om &#x200B;] knoop** te activeren.

   >[!SUCCESS]
   >
   > U hebt het ontwerpen van uw mobiele In-app-bericht nu voltooid. U zou nu op het Overzicht van de Campagne **[!UICONTROL moeten zijn om]** pagina te activeren.
   >
   >![&#x200B; overzicht en activeer &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-4-1-review-and-activate.png)
   >
   > Hier kunt u een volledige samenvatting van uw bericht zien.
   >
   > *gelieve nota te nemen van de douanewaarde die u aangezien u regel teweegbrengt gebruikte. Deze waarde wordt gebruikt om uw bericht in de app te verzenden. De waarde die wordt gebruikt kan op in het hoogtepuntgebied van de summiere pagina worden gevonden.*

   >[!NOTE]
   >De huidige trekker voor het in-app bericht is de standaard **lanceringsgebeurtenis van de Toepassing gebeurt**, zo betekent het dat het in-app bericht wordt teweeggebracht wanneer app lanceert. U kunt dit in de **[!UICONTROL sectie van het Programma zien]**.

5. Als u klaar bent met het evalueren van uw Campagne, druk de Activate knoop om de Campagne te publiceren.
   <br>
   ![&#x200B; activeer &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-4-2-activate.png)


>[!SUCCESS]
>
> Nu moet u het dashboard Campagnes zien. Zoek uw campagne door te schuiven of met de zoekfunctie. Wanneer uw Campagne status in **[!UICONTROL Levend]** (~1min) verandert, is uw Campagne nu gepubliceerd.
>
> ![&#x200B; Gepubliceerde campagne &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-2-published-campaign.png)
>


## Oefening 2.4 Het mobiele bericht in de app activeren

Om de lading te verfrissen en uw onlangs gepubliceerde Campagne te downloaden:

1. Sluit de Fréscopa-app volledig af op uw mobiele apparaat.
2. Open de Fréscopa-app opnieuw.
3. Navigeer nu naar het tabblad Uitoefening in de app.

   ![&#x200B; Uitoefening knoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-3-app-exercise-button.png)

4. Typ in het tekstveld de aangepaste triggerwaarde die u in de campagne hebt gedefinieerd. Druk vervolgens op Verzenden.


   ![&#x200B; wijzigt &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-2-1-app-condition.PNG){width="250" align="center" zoomable="yes"}

>[!SUCCESS]
>
>Door op Verzenden te klikken, hebt u handmatig een trigger geactiveerd en verschijnt het bericht in de app dat u hebt gemaakt:
>
>![&#x200B; In-app bericht &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-1-3-3-in-app-message.png)
>
> *als u kwesties hebt die uw bericht teweegbrengen, controleer het volgende:*
> 
> * *op het de naamgebied van de Gebeurtenis op uw mobiele app, zorg ervoor dat u in uw waarde van de trekkerregel precies typt hoe u het in de Campagne had.*
> * *zorg ervoor kapitalisatie correct is en dat u geen belangrijke of beëindigende ruimte hebt.*
> * *u kunt uw waarde van de trekkerregel opzoeken die u gebruikte als u terug naar uw de overzichtspagina van de Campagne door terug in uw campagne op het Dashboard van de Campagne te klikken gaat.*

U hebt zojuist uw eerste Journey Optimizer In-app-bericht geschreven en gepubliceerd.


## Bonus-oefening: campagne en voorvertoning dupliceren op apparaat

De **Duplicate campagne** en **Voorproef op apparaat** eigenschappen zijn uit-van-de-doosfunctionaliteit die u toestaat om uw Campagnes te dupliceren en uw in-app berichten direct op uw apparaat te testen en te herzien alvorens het te activeren. In deze oefening zult u leren hoe te om deze eigenschap te gebruiken en voorproef het bericht u in oefening 3.1 creeerde.

1. Open de campagne die u net hebt gemaakt door op de naam van de campagne op de pagina Campagnes dashboard te klikken om de campagne te openen. Dit zal u terug naar de **[!UICONTROL campagne van het Overzicht]** pagina nemen.
1. Druk de **[!UICONTROL Dubbele knoop]**. Hiermee wordt een nieuwe aanwijzing geopend voor de naam van de nieuwe campagne die wordt gedupliceerd. Voeg een nieuwe naam toe die u gemakkelijk kunt onthouden of de standaardnaam hebt gebruikt waar **[!DNL _copy]** standaard is toegevoegd.

   ![&#x200B; dubbele campagne &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-2-duplicate-campaign.png)

1. Wanneer u op de knop Dupliceren klikt, wordt de dubbele campagne gemaakt en gaat u terug naar het dashboard Campagnes.
1. Als uw campagne eenmaal is gedupliceerd, opent u uw nieuwe campagne.

1. U kunt tot de Voorproef op apparateneigenschap op de **[!UICONTROL pagina van het overzicht van de Campagne]** toegang hebben of op de **[!UICONTROL de auteur van de Campagne]** stap.

   ![&#x200B; voorproef op apparatenknoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-1-1-preview-on-device-button.png)
   <br>

1. Daarna, klik de **[!UICONTROL beginknoop]** van verbinden met apparatenscherm.

   ![&#x200B; beginknoop &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-1-2-connect-to-device-start.png)
   <br>

1. Voer de basis-URL in die is geconfigureerd om de Fréscopa-app te starten: `dxdemo://`

   ![&#x200B; voorproef url &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-1-3-preview-url.png)

   <br>

1. Volg de instructies op het scherm:
   1. Scan de QR-code met uw mobiele apparaat en de Fréscopa-app wordt geopend met een scherm waarin u een speldenknop kunt weergeven.
   2. Voer het punt in dat in AJO wordt weergegeven op het Assurance-scherm op het apparaat en klik op de knop Connect die rechtsonder wordt weergegeven wanneer u het punt hebt ingevoerd.


   ![&#x200B; ga speld &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-1-5-enter-pin.PNG){width="250" align="center" zoomable="yes"} in
   <br>
1. Deze pop-up verschijnt op uw computerscherm

   ![&#x200B; pop-up &#x200B;](/help/summit-labs/summit-lab-2024/l820-lab-workbook/assets/3-3-pop-up.png)

1. Klik op de knop Gereed. Hierdoor wordt het dialoogvenster gesloten en is uw telefoon nu verbonden met Voorvertonen op apparaat.


>[!SUCCESS]
>
> Uw in-app-bericht wordt op uw apparaat weergegeven.
>
> *Once verbonden, zou uw in-app bericht elke keer moeten tonen, klikt u de **[!UICONTROL Voorproef op apparaat &#x200B;] knoop**.

## Aanvullende bronnen

**hoe te video&#39;s:**

* [Een in-app-campagne maken](/help/channels/create-an-in-app-campaign.md)
* [Een in-app bericht schrijven](/help/channels/author-in-app-messages.md)

**documentatie van het Product:**

* [&#x200B; worden begonnen met in-app kanaal &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/in-app/get-started-in-app)
* [&#x200B; creeer een Mobiel In-app bericht &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/in-app/create-in-app)
* [&#x200B; Ontwerp uw inhoud in-app &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/in-app/design-in-app)
* [&#x200B; Controle en verzend uw bericht In-app &#x200B;](https://experienceleague.adobe.com/nl/docs/journey-optimizer/using/in-app/send-in-app)
