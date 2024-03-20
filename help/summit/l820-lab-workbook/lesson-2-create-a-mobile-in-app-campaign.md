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
source-git-commit: c509c768d07984d07ed2ec65634e000c54bb6ff1
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 0%

---


# Les 2 - Een mobiele campagne in de app maken

In deze les maakt en activeert u mobiele berichten in de app.

## Leerdoelen

* Begrijp hoe in-app berichten worden teweeggebracht.
* Leer hoe u een campagne voor mobiele apparaten in de app maakt.
* Trigger een bericht in de app.

## Oefening 2.1 - Aanmelden bij Journey Optimizer

1. Openen [Adobe Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-ajo-lab/journey-optimizer/home){target="_blank"}
2. Meld u aan met de volgende gegevens:
   <br>
   **Gebruikersnaam:** L820+**`<your seat number>`**@adobeeventlab.com
   **Wachtwoord:**   Adobe 2024!
   <br>
U kunt de details voor uw login op uw bureaublad van de laboratoriummachine vinden. Gebruik de Adobe ID en het Wachtwoord.
   ![desktop](/help/summit/l820-lab-workbook/assets/desk-top.png)

   ![Aanmeldingsscherm](/help/summit/l820-lab-workbook/assets/2-1-1-ajo-sign-in.png)
   <br>
3. U kunt de volgende twee schermen overslaan:
   <br>
   ![Telefoonnummer](/help/summit/l820-lab-workbook/assets/2-1-3-ajo-add-phone.png)
   <br>
   ![Pop-up Personalisatie](/help/summit/l820-lab-workbook/assets/2-1-4-ajo-personalization-pop-up.png)


>[!SUCCESS]
>
>U moet zich aanmelden bij Journey Optimizer en op de startpagina:
>
>![AJO Homepage](/help/summit/l820-lab-workbook/assets/2-1-5-ajo-homepage.png)


## Oefening 2.2 Een mobiele campagne in de app maken

In deze oefening, creeert u een binnen-app overseinencampagne, die wordt teweeggebracht, wanneer u app opent.

1. Selecteer in Journey Optimizer in de linkernavigatie de optie **[!UICONTROL Campagnes]**.

1. Klikken **[!UICONTROL Campagne maken]**.

   ![Campagne maken](/help/summit/l820-lab-workbook/assets/2-3-1-1-create-campaign.png)

1. Op de **[!UICONTROL Campagne maken]** pagina, in de  **[!UICONTROL Handeling]** selecteert u de **[!UICONTROL Bericht in de app]** selectievakje.

1. Van de **[!UICONTROL Verzenden naar]** vervolgkeuzelijst, selecteren **[!DNL Mobile]**.

1. Van de **[!UICONTROL App-oppervlak]** vervolgkeuzelijst, selecteren **[!DNL Frecopa Mobile App]**.

1. Klikken **[!UICONTROL Maken]**.

   ![App-oppervlak](/help/summit/l820-lab-workbook/assets/3-1-1-1-create.png)

>[!SUCCESS]
>
>U moet nu op de eigenschappen van de Campagne staan:
>
> ![Campagneigenschappen](/help/summit/l820-lab-workbook/assets/3-1-1-2-campaign-properties.png)

## Oefening 2.3 Uw campagne configureren

### 2.3.1. [!UICONTROL Sectie Eigenschappen]

Geef uw campagne een naam. Zorg ervoor dat u de naam met het nummer van uw licentie start, zodat u de campagne eenvoudig opnieuw kunt vinden.

Als uw nummer bijvoorbeeld 99 is:  `99 - Welcome Campaign`.

![sectie Eigenschappen](/help/summit/l820-lab-workbook/assets/3-1-2-1-properties-section.png)

### 2.3.2 De aangepaste triggerregel instellen

1. Omlaag schuiven naar de **[!UICONTROL Sectie Triggers]** en klik vervolgens op **[!UICONTROL Triggers bewerken]**.

   ![wijzigen](/help/summit/l820-lab-workbook/assets/3-2-1-2-edit-triggers.png)

1. Klik in de regelbouwer op **[!UICONTROL Toepassing starten]** en vanuit de vervolgkeuzelijst selecteert u  *Gegevens verzonden naar platform*.
   ![Verzonden naar gegevensplatform](/help/summit/l820-lab-workbook/assets/trigger-drop-down-sent-to-platform.png)

1. Voeg een voorwaarde toe door te klikken **[!UICONTROL Voorwaarde toevoegen]**.

   ![knop voor toevoegen aan voorwaarde](/help/summit/l820-lab-workbook/assets/3-2-1-3-add-condition.png)

1. Van de **[!UICONTROL Een kenmerk selecteren]** vervolgkeuzelijst, selecteren **[!UICONTROL XDM-gebeurtenistype]**.

   ![XDM-gebeurtenistype](/help/summit/l820-lab-workbook/assets/4-1-2-dropdown-xdm-event.png)

1. Voeg in het volgende tekstveld een *`<custom string value>`* dat u zich kunt herinneren.

1. Klik op ** om de waarde op te slaan[!UICONTROL Toevoegen**] `<custom string value>`.

   Deze aangepaste tekenreekswaarde wordt later gebruikt om uw bericht te verzenden.

   >[!TIP]
   > Door het nummer van uw licentie toe te voegen aan de aangepaste tekenreekswaarde, kunt u deze uniek en gemakkelijker onthouden.
   > 
   > Bijvoorbeeld: `99exerciseTrigger`

   ![aangepaste tekenreekswaarde voor trigger toevoegen](/help/summit/l820-lab-workbook/assets/3-1-2-2-add-custom-trigger.png)

1. Klikken **[!UICONTROL Gereed]** rechtsboven.

>[!SUCCESS]
>
>U hebt nu uw bericht in de app gedefinieerd met een aangepaste triggergebeurtenis.
>
>![Campagne met aangepaste trigger gedefinieerd](/help/summit/l820-lab-workbook/assets/3-1-2-2-campaign-with-custom-trigger.png)


### 2.3.3 De inhoud van het bericht in de app bewerken

In de **[!UICONTROL Handeling]** sectie, klikken **[!UICONTROL Inhoud bewerken]**.

![Knop Inhoud bewerken](/help/summit/l820-lab-workbook/assets/3-1-3-1-edit-content-button.png)

De [!UICONTROL Bericht in de app] de vertoningen van de redacteur, waar u de in-app berichtinhoud vormt.

#### 2.3.3.1 Layout

Selecteer welke lay-out op uw bericht zou moeten worden toegepast.

Klik bijvoorbeeld op **[!UICONTROL Modal]** om van uw in-app bericht een modale lay-out te maken.

![modale knop](/help/summit/l820-lab-workbook/assets/3-1-3-2-modal-button.png)

#### 2.3.3.2 Uw boodschap schrijven en uw campagne publiceren

1. Plak in de sectie Media in de volgende URL:  `https://t3.ftcdn.net/jpg/02/79/42/52/240_F_279425217_Hr9VBkknMr4fTpuZbxZXfcYdC7jSvGl2.jpg`
   <br>
Wanneer u buiten het waardeveld klikt, wordt de afbeelding weergegeven.

   ![media weergegeven in de voorvertoning](/help/summit/l820-lab-workbook/assets/3-1-3-2-media.png)

2. In het volgende **[!UICONTROL Inhoud]** , voegt u in uw eigen aangepaste tekst toe die u in uw bericht voor de **[!UICONTROL Koptekst]** en **[!UICONTROL Lichaam]**.

   ![Koptekst en tekst](/help/summit/l820-lab-workbook/assets/3-1-3-2-content.png)

3. Aanvullende opties:
   1. **Knoppen:**

      ![Knopsectie](/help/summit/l820-lab-workbook/assets/3-1-3-2-buttons.png)

      1. In deze sectie van de redacteur, kunt u de tekst voor uw knoop aanpassen CTA door het gebied van de Tekst van de Knoop uit te geven.

      2. De **[!UICONTROL Interactie]** wordt gebruikt om de waarde te bepalen die aan SDK wordt overgegaan wanneer CTA door de gebruiker wordt gedrukt.

      3. De **[!UICONTROL Doel]** wordt gebruikt om te bepalen waar u CTA de gebruiker wilt nemen. Dit omvat URLs en Deplinks. U kunt deze koppeling bijvoorbeeld toevoegen aan een productpagina, zoals `dxdemo://exoticVibes`.

      4. U kunt extra knoppen toevoegen door op **[!UICONTROL + Knop Toevoegen]**.

      5. Wanneer een tweede knoop aan uw bericht wordt toegevoegd, hebt u nu de optie om de knooplay-out met de drop-down doos te veranderen.


   2. **Geavanceerde opmaak**

      ![schakelen tussen geavanceerde opmaak](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-toggle.png)

      Als u deze schakeloptie inschakelt, krijgt u extra aanpassingsopties in de editor.

      1. Mediaformaat
      1. Lettertype
      1. Pt-grootte
      1. Lettertypekleur
      1. Uitlijning

      ![geavanceerde opmaakopties](/help/summit/l820-lab-workbook/assets/3-1-3-2-advanced-formatting-options.png)

   3. **Tabblad Instellingen**

      Door over te gaan naar dit lusje en in **[!UICONTROL Voorvertoning]** kunt u de **App-voorvertoning**.
      <br>\
      ![Het tabblad Instellingen](/help/summit/l820-lab-workbook/assets/3-1-3-1-settings-tab.png)
      <br>

      1. De **[!UICONTROL Layout]** kunt u een afbeelding gebruiken als achtergrond of als een effen kleur.

      2. De **[!UICONTROL Bericht]** Deze sectie biedt aangepaste interacties die voor uw bericht kunnen worden ingeschakeld:
         1. Aangepaste bewegingen
         2. UI-overname
         3. Aangepaste UI-overname
         4. Aangepaste grootte
         5. Aangepaste positie
         6. Aangepaste animatie
         7. Hoek voor bericht
   <br>
4. Wanneer u klaar bent met het ontwerpen van de inhoud en tevreden bent met uw bericht, klikt u op de knop **[!UICONTROL Controleren om te activeren] knop**.

   >[!SUCCESS]
   >
   > U hebt het ontwerpen van uw mobiele In-app-bericht nu voltooid. U moet nu aan de Campagne deelnemen **[!UICONTROL Controleren om te activeren]** pagina.
   >
   >![revisie en activeren](/help/summit/l820-lab-workbook/assets/3-1-4-1-review-and-activate.png)
   >
   > Hier kunt u een volledige samenvatting van uw bericht zien.
   >
   > *Houd rekening met de aangepaste waarde die u hebt gebruikt als triggerregel. Deze waarde wordt gebruikt om uw bericht in de app te verzenden. De gebruikte waarde vindt u in het hooglichtgebied van de overzichtspagina.*

   >[!NOTE]
   >De huidige trigger voor het bericht in de app is de standaardtrigger **Gebeurtenis voor starten van toepassing**, wat betekent dat het bericht in de app wordt geactiveerd wanneer de app wordt gestart. U kunt dit zien in de **[!UICONTROL Sectie Schema]**.

5. Als u klaar bent met het evalueren van uw Campagne, druk de Activate knoop om de Campagne te publiceren.
   <br>
   ![activate](/help/summit/l820-lab-workbook/assets/3-1-4-2-activate.png)


>[!SUCCESS]
>
> Nu moet u het dashboard Campagnes zien. Zoek uw campagne door te schuiven of met de zoekfunctie. Wanneer uw campagne de status wijzigt in **[!UICONTROL Live]** (~1 min) is uw campagne nu gepubliceerd.
>
> ![Gepubliceerde campagne](/help/summit/l820-lab-workbook/assets/3-1-3-2-published-campaign.png)
>


## Oefening 2.4 Het mobiele bericht in de app activeren

Om de lading te verfrissen en uw onlangs gepubliceerde Campagne te downloaden:

1. Sluit de Fréscopa-app volledig af op uw mobiele apparaat.
2. Open de Fréscopa-app opnieuw.
3. Navigeer nu naar het tabblad Uitoefening in de app.

   ![Oefening, knop](/help/summit/l820-lab-workbook/assets/3-2-3-app-exercise-button.png)

4. Typ in het tekstveld de aangepaste triggerwaarde die u in de campagne hebt gedefinieerd. Druk vervolgens op Verzenden.


   ![wijzigen](/help/summit/l820-lab-workbook/assets/3-2-2-1-app-condition.PNG){width="250" align="center" zoomable="yes"}

>[!SUCCESS]
>
>Door op Verzenden te klikken, hebt u handmatig een trigger geactiveerd en verschijnt het bericht in de app dat u hebt gemaakt:
>
>![Bericht in de app](/help/summit/l820-lab-workbook/assets/3-1-3-3-in-app-message.png)
>
> *Als u problemen hebt die uw bericht veroorzaken, controleer het volgende:*
> 
> * *Controleer in het veld Gebeurtenisnaam op uw mobiele app of u de waarde van de triggerregel exact opgeeft zoals deze in de campagne staat.*
> * *Zorg ervoor dat het hoofdlettergebruik correct is en dat u geen voorloopruimte of eindruimte hebt.*
> * *U kunt de waarde van de triggerregel opzoeken die u hebt gebruikt als u teruggaat naar de pagina van de campagneoverzicht door weer op het campagnedashboard te klikken.*

U hebt zojuist uw eerste Journey Optimizer In-app-bericht geschreven en gepubliceerd.


## Bonus-oefening: campagne en voorvertoning dupliceren op apparaat

De **campagne dupliceren** en **Voorvertonen op apparaat** -functies zijn functies die u kunt uitschakelen, zodat u uw campagnes kunt dupliceren en uw in-app-berichten rechtstreeks op uw apparaat kunt testen en bekijken voordat u deze activeert. In deze oefening zult u leren hoe te om deze eigenschap te gebruiken en voorproef het bericht u in oefening 3.1 creeerde.

1. Open de campagne die u net hebt gemaakt door op de naam van de campagne op de pagina Campagnes dashboard te klikken om de campagne te openen. Hiermee gaat u terug naar de **[!UICONTROL Revisiecampagne]** pagina.
1. Druk op **[!UICONTROL Knop Dupliceren]**. Hiermee wordt een nieuwe aanwijzing geopend voor de naam van de nieuwe campagne die wordt gedupliceerd. Voeg een nieuwe naam toe die u gemakkelijk herinnert of gebruikte standaardnaam waar **[!DNL _copy]** wordt standaard toegevoegd.

   ![dubbele campagne](/help/summit/l820-lab-workbook/assets/3-2-duplicate-campaign.png)

1. Wanneer u op de knop Dupliceren klikt, wordt de dubbele campagne gemaakt en gaat u terug naar het dashboard Campagnes.
1. Als uw campagne eenmaal is gedupliceerd, opent u uw nieuwe campagne.

1. U kunt de functie Voorvertonen op apparaat openen op het tabblad **[!UICONTROL Campagneoverzicht]** of op de **[!UICONTROL Campagneontwikkelaar]** stap.

   ![voorvertoning op apparaatknop](/help/summit/l820-lab-workbook/assets/3-3-1-1-preview-on-device-button.png)
   <br>

1. Klik op de knop **[!UICONTROL startknop]** via het scherm Verbinding maken met apparaat.

   ![startknop](/help/summit/l820-lab-workbook/assets/3-3-1-2-connect-to-device-start.png)
   <br>

1. Voer de basis-URL in die is geconfigureerd om de Fréscopa-app te starten: `dxdemo://`

   ![voorbeeld-URL](/help/summit/l820-lab-workbook/assets/3-3-1-3-preview-url.png)

   <br>

1. Volg de instructies op het scherm:
   1. Scan de QR-code met uw mobiele apparaat en de Fréscopa-app wordt geopend met een scherm waarin u een speldenknop kunt weergeven.
   2. Voer het punt in dat in AJO wordt weergegeven op het scherm Verzekering op uw apparaat en klik op de knop Verbinden die rechtsonder wordt weergegeven wanneer u het punt hebt ingevoerd.


   ![punt invoeren](/help/summit/l820-lab-workbook/assets/3-3-1-5-enter-pin.PNG){width="250" align="center" zoomable="yes"}
   <br>
1. Deze pop-up verschijnt op uw computerscherm

   ![pop-up](/help/summit/l820-lab-workbook/assets/3-3-pop-up.png)

1. Klik op de knop Gereed. Hierdoor wordt het dialoogvenster gesloten en is uw telefoon nu verbonden met Voorvertonen op apparaat.


>[!SUCCESS]
>
> Uw in-app-bericht wordt op uw apparaat weergegeven.
>
> *Wanneer de verbinding tot stand is gebracht, wordt het bericht in de app elke keer weergegeven en klikt u op de knop **[!UICONTROL Voorvertonen op apparaat] knop**.*