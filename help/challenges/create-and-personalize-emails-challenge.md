---
title: Berichten maken en personaliseren
description: Test uw kennis over het maken en personaliseren van e-mails.
kt: 7531
feature: Journeys
role: User
level: Beginner
source-git-commit: 676f0b268f7f67d179bfa944b72cb68191640c74
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---


# Berichten maken en personaliseren

## Het artikel

Luma, een fictioneel atletisch kledingbedrijf, wil zijn nieuwste kleding- en tandwielcollectie promoten en de verkoop voor bestaande klanten stimuleren. Om de Nieuwe campagne van de Inzameling te steunen, vraagt het marketing team van Luma u om twee e-mailberichten tot stand te brengen die naar klanten als deel van de campagne worden verzonden.

## Uw uitdaging

De volgende e-mails maken in Journey Optimizer

### E-mailbericht #1 - Aankondiging van de zomerverzameling

Maak een e-mail om de komst van de nieuwe zomerverzameling aan te kondigen. U hebt een HTML-bestand ontvangen van een bureau met het ontwerp van de e-mailtekst: [SeasonalCollectionEmail.html](/help/challenges/assets/SeasonalCollectionEmail.html)

1. Een e-mailbericht maken met de naam *(uw naam)_Luma - Nieuwe seizoensverzameling*
2. Geef de e-mail een onderwerpregel: *(voornaam van ontvanger), is de nieuwe verzameling Luma hier!*
3. Het opgegeven HTML-bestand gebruiken voor de hoofdtekst van de e-mail  

SUCCESCRITERIA

Geef een voorbeeld van het e-mailbericht weer met uw testprofiel en stuur een proefdruk naar uzelf.

* De onderwerpregel moet uw naam erin hebben
* De hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien.

### E-mailbericht nr. 2 - E-mailbericht voor bevestiging van bestelling

Maak een bevestigingsbericht voor bestellingen dat moet worden verzonden wanneer een klant van een luminantie een onlinebestelling voltooit.  

1. Maak een e-mailbericht met de naam &quot;(uw naam)_ Luma - Bestelbevestiging&quot;
2. De onderwerpregel moet worden gepersonaliseerd met de voornaam van de ontvanger en de uitdrukking &quot;bedankt voor uw aankoop&quot; bevatten
3. Overeenkomstig de merkenrichtlijn van Luma moet de e-mail als volgt worden gestructureerd:
   * Koptekst:
      * Logo luminantie (Luma_Logo.png)
      * Grootte 35%, gecentreerde witte achtergrond  
      * De website moet een link hebben naar de lumawebsite: ```https://publish1034.adobedemo.com/content/luma/us/en.html``` 
   * Hoofdgedeelte 1:  
      * Afbeelding:  
         * Luma - Transactie - Bestelbevestiging 2.jpg
         * Marge: Boven, onder (10)
      * Tekst:
         * Kop: &quot;Bedankt voor uw aankoop!&quot;
         * Body: &quot;Uw bestelling is geplaatst. Zodra uw pakket is verzonden, sturen we u een e-mail met een trackingnummer, zodat u uw bestelling kunt volgen.&quot;
         * Uitlijning: left  
         * Opvulling: links(95), rechts (95)
      * Een knop: &quot;Bekijk uw bestelling&quot;
         * Achtergrondkleur: rgb (25, 121, 195)
         * Tekstkleur: rgb (101, 106, 119); tekengrootte: 14 px
         * Geen rand 
         * Hoogte: 40 
         * Een koppeling toevoegen aan een door u gekozen website  
         * Links uitlijnen met de bovenstaande tekst (tip: de containermarge gebruiken)
      * Een scheidingslijn:
         * Lijnkleur: #d3d3d3 rgb (211, 211, 211)
      * Tekst:
         * *Wij zijn hier om u te helpen. Als u vragen hebt, of hulp nodig hebt, laat het ons weten.*
         * *Laat ons weten* zou een verbinding aan de steun email: support.luma@emailcim.io moeten hebben  
   * Hoofdgedeelte 2: Bestelgegevens met de volgende contextafhankelijke informatie
      * Koptekst: inkoopordernummer
      * Lijst met bestelde producten
      * Totale productprijs
      * Productnaam
      * Producthoeveelheid
      * Totale prijs van de order
   * Hoofdgedeelte 3: Klantgegevens
      * Klantgegevens koptekst
      * Verzending (voornaam, achternaam, straat1, plaats) en factuuradres (voornaam, achternaam, straat1, plaats), die naast elkaar moeten worden vermeld (tip: twee kolommen toevoegen voor deze sectie). De gegevens moeten in het klantprofiel worden ingevuld.  
   * Voettekst
      * Koppelingen naar Facebook en LinkedIn via sociale media
      * Koppeling voor abonnement opzeggen
      * Tekstkleur: #afafafaf rgb (175, 175, 175)

>[!IMPORTANT]
>
>De sectie met orderdetails bevat contextuele gebeurtenisinformatie. Het is alleen mogelijk om contextuele informatie toe te voegen zodra het bericht aan een werkstroom is toegevoegd. Publiceer de e-mail niet voordat u deze aan de workflow hebt toegevoegd en hebt gewijzigd met de contextuele gebeurtenisinformatie. Gebruik ook de hulpfunctie.

1. Een reis maken die wordt geactiveerd wanneer een klant een onlineaankoop op de Luma-website voltooit en de *(uw naam)_ Luma - Website - Bevestiging van bestelling* email

   * Roep de reis &quot;uw naam _Luma-Order Bevestiging&quot;
   * De gebeurtenis gebruiken: LumaOnlinePurchase  

SUCCESCRITERIA

1. Geef een voorvertoning van uw bericht weer met het testprofiel dat u hebt gemaakt. De personalisatie moet de gegevens in uw testprofiel weerspiegelen:  
   * De onderwerpregel moet beginnen met de voornaam van het testprofiel 
   * De klanteninformatie zou de voornaam en achternaam van uw testprofiel, en de stad moeten hebben. Als u het adres van de straat hebt toegevoegd, wordt het weergegeven als dat veld niet leeg blijft. 
2. Publiceer de e-mail en verzend het naar zich door de reis te leiden u in testwijze creeerde: 
   * Selecteer het gebeurtenistype &quot;commerce.purchase&quot; 
   * Gebruik &quot;LLWH06&quot; voor de product-SKU wanneer u de testgebeurtenis in de testmodus activeert.  
   * Aanvullende informatie toevoegen  
   * URL afbeelding: https://publish1034.adobedemo.com/content/dam/luma/en/products/women/tops/hoodies-&amp;-sweatshirts/wh06-purple_main.jpg 
   * U ontvangt het e-mailbericht en alle velden voor personalisatie moeten correct worden ingevuld.

KLAAR OM TE EINDIGEN?

[Uw werk controleren](/help/challenges/check-your-work/create-and-personalize-emails.md) om te zien hoe de e-mails die u hebt gemaakt er moeten uitzien.
