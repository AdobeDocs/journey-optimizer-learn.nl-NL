---
title: Reis maken
description: Een reis maken die wordt geactiveerd bij de gebeurtenis price.drop
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Reis maken

In deze stap maakt u een reis in Adobe Journey Optimizer die wordt geactiveerd door de gebeurtenis custom price.drop. Wanneer deze gebeurtenis wordt ontvangen, begint de reis in real time en verzendt een dupbericht naar gebruikers die hebben gekozen binnen, toelatend gebeurtenis-gedreven betrokkenheid.

Volg de volgende stappen om een reis te maken die wordt geactiveerd bij de gebeurtenis price.drop

* Aanmelden bij Journey Optimizer
* Navigeren naar Reisbeheer | Reis maken | Reis maken

![&#x200B; creeer-reis &#x200B;](assets/create-journey.png)

## PriceDropEvent toevoegen

Sleep de `PriceDropEvent` van de gebeurtenissensectie naar het canvas
![&#x200B; prijs-drop-event &#x200B;](assets/add-price-drop-event.png)

## Drukhandeling toevoegen

Vouw de sectie Handelingen uit. Sleep de `Action` -activiteit naar het canvas en selecteer Duwen als actietype
![&#x200B; duw-actie &#x200B;](assets/add-push-action.png)

## De pushactie configureren

Selecteer de activiteit van de dupmelding en klik op vormen actie

![&#x200B; vorm-duw-actie &#x200B;](assets/configure-push-action.png)

## Configuratie van pushmeldingskanaal

Koppel `MyFirstWebPushChannel` configuratie die eerder in de zelfstudie is gemaakt aan deze pushmelding

![&#x200B; kanaal-configuratie &#x200B;](assets/journey-actions.png)

## Pushmelding samenstellen

Voeg een combinatie statische en dynamische inhoud aan het dupbericht toe gebruikend de verpersoonlijkingsredacteur om het bericht boeiender en relevanter te maken.

Als u wilt beginnen met het samenstellen van het bericht, klikt u op `Content` om het tabblad Inhoud te openen, waarin u zowel de vaste tekst als de dynamische velden kunt definiëren die zijn afgeleid van de gebeurtenisgegevens.
![&#x200B; inhoud-duw &#x200B;](assets/compose-message.png)

Geef de titel van het pushbericht op en open vervolgens de personalisatie-editor om de berichttekst samen te stellen. De inhoud bevat dynamisch de namen van de producten waarvan de prijzen zijn gedaald. Om dit te bereiken, gebruik de elke [&#x200B; hulpfunctie &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/personalization/functions/helpers#each)
om over de lijst van producten te herhalen en hun namen binnen het bericht terug te geven.

## De berichttekst samenstellen

Selecteer de functie `Each` in het menu met hulpfuncties en voeg deze in.
![&#x200B; helper-functie &#x200B;](assets/journey-content-helper-function.png)

Selecteer de contextafhankelijke kenmerken | Journey Orchestration | Gebeurtenissen | PriceDropEvent | productListItems | Naam

Klik op het pictogram &quot;+&quot; om de array in te voegen in elke lus in de verpersoonlijkingseditor. Werk vervolgens de inhoud van het bericht bij in overeenstemming met de indeling die wordt weergegeven in de schermafbeelding van het referentiescherm. De gebeurtenis-id die in uw omgeving wordt weergegeven, kan afwijken van de id die wordt weergegeven.

![&#x200B; contextafhankelijke-attributen &#x200B;](assets/journey-content-context-attributes.png)

Tot slot sparen al uw veranderingen en publiceer de reis. Zodra gepubliceerd, wordt de reis actief en luistert naar inkomende prijs.drop gebeurtenissen. Telkens wanneer een dergelijke gebeurtenis wordt ontvangen, wordt de reis in real time geactiveerd en wordt een pushmelding verzonden naar gebruikers die ervoor hebben gekozen meldingen te ontvangen, waarbij tijdige en relevante betrokkenheid wordt gewaarborgd.

## De oplossing testen

Om de price.drop gebeurtenis teweeg te brengen, open de [&#x200B; de triggerpagina van de prijsdaling, &#x200B;](http://localhost:3000/price-drop-trigger.html) één of meerdere producten selecteren, en de Daling van de Prijs van de Trekker klikken. Hierdoor wordt de gebeurtenis via de Adobe Data Layer verzonden met AEP Tags, die vervolgens de rit start en de pushmelding in real-time aflevert.



