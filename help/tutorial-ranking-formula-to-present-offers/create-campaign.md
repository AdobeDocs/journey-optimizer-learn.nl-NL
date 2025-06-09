---
title: Een campagne maken
description: Leer hoe een AJO-campagne het publiek, het beslissingsbeleid en de kanalen verbindt om persoonlijke aanbiedingen op het juiste moment aan te bieden via de verschillende aanraakpunten van de klant.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18188
exl-id: deb16dd5-23cd-495a-ac91-d22fd77f49bd
source-git-commit: 7d812f589172c5052a1e9bfcf6a99d0769a6c2c7
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 1%

---

# Een campagne maken

Om gepersonaliseerde aanbiedingen aan gebruikers op de Web-pagina te leveren, werd een campagne gecreeerd in Adobe Journey Optimizer en gevormd met het correcte kanaal, Webkanaal. Deze configuratie zorgt ervoor dat de aanbiedingen via real-time besluitvorming worden geleverd aan gebruikers die met de website communiceren.

Binnen deze campagne werd een beslissingsbeleid gedefinieerd om te bepalen hoe aanbiedingen worden geselecteerd. Het besluitvormingsbeleid omvat een selectiestrategie die bestaat uit:

Een verzameling van aanbiedingsitems (bijvoorbeeld op basis van postcode of inkomen);

Geschiktheidsregels die bepalen welke aanbiedingen op een gebruiker van toepassing zijn, en

Een rangschikkingsformule die scores toewijst aan in aanmerking komende aanbiedingen om prioriteit te geven aan de meest relevante aanbiedingen.

Wanneer een aangemelde gebruiker de site bezoekt, wordt een verzoek tot personalisatie naar AJO verzonden. Op basis van de door de gebruiker opgegeven identiteits- en profielkenmerken (zoals postcode en jaarinkomen) beoordeelt het beslissingsbeleid alle beschikbare aanbiedingen. Het past de selectiestrategie en rangschikkingslogica toe om de beste gelijke te bepalen.

Het resultaat is een op maat gemaakte reeks aanbiedingen, die als HTML-inhoud worden geretourneerd en in een carrousel op de website worden weergegeven, waardoor een naadloze, realtime persoonlijke ervaring ontstaat.


## Stappen op hoog niveau om een campagne te maken in AJO

1. **creeer een Configuratie van het Kanaal**\
   Bepaal waar en hoe de aanbiedingen worden weergegeven (bijvoorbeeld een webpagina met ervaring in code).
   - Aanmelden bij Reisoptimzer
Ga naar Beheer ->Kanalen ->Kanaalconfiguratie maken
   - **Naam**: `finwise-web-personalization`\
     Identificeert deze configuratie voor de gepersonaliseerde levering van de Webaanbieding van FinWise.

   - **Platform**: `Web`\
     Specifiek gericht op webbrowsers. Er zijn geen mobiele kanalen ingeschakeld.

   - **Type van Ervaring**: `Code-based experience`\
     Aanbiedingen worden niet rechtstreeks in het DOM geïnjecteerd. In plaats daarvan retourneert AJO raw HTML dat wordt geparseerd met behulp van aangepaste JavaScript.

   - **pagina URL**: `http://localhost:3000/formula.html`\
     Het kanaal wordt gevormd voor een specifieke testpagina die tijdens ontwikkeling wordt gebruikt.

   - **Plaats op Pagina**: `offers-div`\
     Geretourneerde aanbiedingen worden dynamisch geparseerd en in deze container gerenderd met behulp van frontend-logica.

   - **Formaat van de Inhoud**: `HTML`\
     De aanbiedingen worden geleverd als onbewerkte HTML-fragmenten, zodat u volledige controle hebt over de stijl, filtering en weergave van de fragmenten.


2. **Begin een Nieuwe Campagne**\
   Navigeer naar de sectie Campagnes en maak een nieuwe geplande marketingcampagne. Geef de campagne een relevante naam.


3. **voeg Actie** toe\
   Voeg op code-gebaseerde-ervaring actie toe en verbind de actie met een eerder gecreeerde kanaalconfiguratie.



4. **Doelgroep**\
   Alle bezoekers (standaard).

   Identiteitstype: ECID (Experience Cloud-id)
Deze instelling gebruikt de ECID als primaire identiteit voor het herkennen van gebruikers. Wanneer identiteitsstitching op zijn plaats is, wordt ECID verbonden met CRM identiteitskaart voor Personalized Targeting Uitgezochte of creeert een besluitvormingsbeleid dat de aanbiedingslogica bepaalt.

5. **Beleid van het Besluit**


   De actie is verbonden met het Beleid van het a **Besluit** dat bepaalt hoe de aanbiedingen worden geselecteerd en hoeveel aanbiedingen voor vertoning zijn teruggekeerd. Dit beleid gebruikt a **Strategie van de Selectie** die vroeger in het leerprogramma werd gecreeerd.

   Om het besluitvormingsbeleid op te nemen geeft de klik **_inhoud_** in de secties van Acties uit en klikt dan **_code_** uit om de verpersoonlijkingsredacteur te openen.

   Selecteer _&#x200B;**pictogram van het Beleid van het Besluit**&#x200B;_ op de linkerzijde en klik op **voeg besluitvormingsbeleid** knoop toe om **te openen creeer besluitvormingsbeleid** scherm. Geef het beslissingsbeleid een betekenisvolle naam en selecteer het aantal items dat het beslissingsbeleid moet retourneren. De standaardwaarde is 1.
Klik **_volgende_**, en voeg de selectiestrategie toe die in de vroegere stap aan het besluitvormingsbeleid wordt gecreeerd en klik **daarna** om het proces te voltooien om het besluitvormingsbeleid te creëren. Selecteer de gewenste fallback-aanbieding.

6. **Tussenvoegsel het Beleid van het Besluit**

   ![ verpersoonlijking-redacteur ](assets/personalization-editor.png)

   Tussenvoegsel het onlangs gecreeerde besluitvormingsbeleid door op de _&#x200B;**knoop van het Beleid van het Tussenvoegsel**&#x200B;_ te klikken. Dit neemt een for lijn in de verpersoonlijkingsredacteur aan de rechterkant op.
Plaats de cursor tussen de lus op regel twee en voeg de offerText in door naar het aanbod te navigeren door naar de lus te gaan door de `tenant name` omlaag te boren


   De code Handlebars doorloopt de aanbiedingen die door een specifiek besluitvormingsbeleid in Adobe Journey Optimizer zijn teruggekeerd en leidt tot een `<div>` voor elke aanbieding. Elke `<div>` gebruikt een attribuut data-tags met de interne naam van de aanbieding om de carrouselgroep te helpen en aanbiedingen per categorie te ordenen voor vloeiende navigatie. De inhoud binnen elke `<div>` geeft de tekst van de gepersonaliseerde aanbieding weer, waardoor een dynamische en visueel gesegmenteerde presentatie van meerdere aanbiedingen mogelijk is.


7. **publiceer de Campagne**\
   Activeer de campagne om persoonlijke aanbiedingen in real-time te leveren.

![ img ](assets/personalization-editor.png)
