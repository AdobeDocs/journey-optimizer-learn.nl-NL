---
title: De oplossing testen
description: Maak een eenvoudige webpagina om de context te testen en maak personalisatie mogelijk met behulp van real-time temperatuurgegevens.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: 609a5ddf-d6c6-4f19-bd7f-bca8c266b759
source-git-commit: 23832f2e59ca7558fd403f0a9753db3923023e6d
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# De oplossing testen

Om de oplossing van begin tot eind te testen, moeten [ weer-aanbiedingen.html ](assets/weather-offers.html) en [ weer-verwant-aanbiedingen-script.js ](assets/weather-related-offers-script.js) dossiers op een Webserver of een openbare ontvangende dienst zoals de Pagina&#39;s van Github worden ontvangen. Dit is nodig omdat:
- De geolocatie-API van de browser werkt alleen via HTTPS of localhost

Om de zaken georganiseerd te houden en relatieve wegen te verzekeren werken correct, adviseren wij de volgende omslagstructuur voor het ontvangen van de oplossing:

![ omslag-structuur ](assets/folder-structure.png)

## Beschikbare bestanden downloaden

[HTML-bestand](assets/weather-offers.html)

[JavaScript-bestand](assets/weather-related-offers-script.js)


## De URL van het oppervlak in het JavaScript-bestand bijwerken

Open `weather-related-offers-script.js` en werk ` "web://yourdomain.com/weather/weather-offers.html#offerContainer"` bt die `yourdomain.com` vervangt met het daadwerkelijke domein bij waar het dossier van HTML wordt ontvangen.

## De eigenschap Adobe Experience Platform-tags bijwerken

Open het bestand weer-aanbiedingen.html in de teksteditor en vervang de scripttag door de scripttag van de Adobe Experience Platform-tageigenschap die u in de vorige stap van deze zelfstudie hebt gemaakt. Sla het bestand op

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```



## Wat de webpagina doet

Er is een webpagina gemaakt voor het testen van contextafhankelijk maken van functies met behulp van real-time temperatuurgegevens. Wanneer een gebruiker de pagina bezoekt, vraagt de browser om toegang tot de geolocatie. Op goedkeuring, haalt de pagina de huidige weerdetails-zoals temperatuur, voorwaarde, en stad-via OpenWeatherMap API. Deze contextuele gegevens worden weergegeven aan de gebruiker en naar Adobe Experience Platform verzonden met de Adobe Web SDK (Alloy).

De sendEvent vraag wordt gevormd met renderDecisions: vals, betekenend aanbiedingen die door Adobe Journey Optimizer zijn teruggekeerd worden manueel behandeld. Het manuscript verwerkt de beslissingsreactie, decodeert de inhoud, en neemt dynamisch de meest relevante aanbieding in een aangewezen container (#offerContainer) op.

## Wat de JavaScript doet

De JavaScript haalt dynamisch weerinformatie op op basis van de locatie van de gebruiker en gebruikt Adobe Experience Platform (AEP) om persoonlijke aanbiedingen te leveren. Hier volgt een overzicht van de stappen:

1. **wacht op Alloy om** te laden

   Het script zorgt ervoor dat de Adobe Web SDK (Alloy) volledig is geladen voordat er een verzoek tot personalisatie wordt ingediend.

2. **krijgt de Plaats van de Gebruiker**

   De Geolocation-API van de browser wordt gebruikt om de huidige breedte en lengte van de gebruiker op te halen.

3. **de Gegevens van het Weer van Vetsen**

   De OpenWeatherMap-API wordt aangeroepen om actuele weerdetails op te halen:

   Temperatuur (in °F)

   Weergavevoorwaarde (bijvoorbeeld &quot;Regen&quot;, &quot;Wissen&quot;)

   Plaats

   Vochtigheid

4. **Info van het Weefsel van de Vertoning op de Web-pagina**

   Werkt het DOM bij met een bericht als:

   &quot;De huidige temperatuur in San Diego is 72°F met heldere luchten.&quot;

5. **verzendt Weer Context aan AEP**

   Gebruikt legering(&quot;sendEvent&quot;) om contextafhankelijke weergegevens naar AEP te verzenden

   ```javascript
   xdm: {
   eventType: "decisioning.request",
   _techmarketingdemos: {
   temperature: temp,
   weatherConditions: condition,
   cityName: city
     }
   }
   ```

6. **wint en geeft Aanbiedingen terug**

   Ontvangt voorstellen die door AJO zijn geretourneerd.

   Decodeert de HTML-inhoud.

   Injecteert de aanbiedingen dynamisch in de <div id="offerContainer"> element.

