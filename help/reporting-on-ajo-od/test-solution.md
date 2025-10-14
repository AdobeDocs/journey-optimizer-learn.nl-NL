---
title: De oplossing testen
description: Maak een eenvoudige webpagina om indruk te maken en klik op gebeurtenissen voor de aanbiedingen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-07-18T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18526
source-git-commit: 69bc8aace3cc502a18e691584824176833413c7e
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# De oplossing testen

Om de oplossing van begin tot eind te testen, moeten [&#x200B; weer-aanbiedingen.html &#x200B;](assets/weather-offers.html) en [&#x200B; vangst-impressions-klik-events.js &#x200B;](assets/capture-impressions-click-events.js) dossiers op een Webserver of een openbare ontvangende dienst zoals de Pagina&#39;s van Github worden ontvangen. Dit is nodig omdat de geolocatie-API van de browser alleen werkt via HTTPS of localhost

## Beschikbare bestanden downloaden

[HTML-bestand](assets/weather-offers.html)

[JavaScript-bestand](assets/capture-impressions-click-events.js)

## De URL van het oppervlak in het JavaScript-bestand bijwerken

Open `capture-impressions-click-events.js` en werk ` "web://yourdomain.com/weather/weather-offers.html#offerContainer"` bij door `yourdomain.com` met het daadwerkelijke domein te vervangen waar het dossier van HTML wordt ontvangen.


## De eigenschap Adobe Experience Platform-tags bijwerken

Open het bestand weer-aanbiedingen.html in de teksteditor en vervang de scripttag door de scripttag van de Adobe Experience Platform-tageigenschap die u in de vorige stap van deze zelfstudie hebt gemaakt. Sla het bestand op

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```

## Interactie met de aanbiedingen

- Open de webpagina in uw favoriete browser.

- Toestaan _&#x200B;**plaats het volgen**&#x200B;_. Dit is vereist om de weerdetails op basis van uw locatie te krijgen.

- Klik op de knop in de aanbiedingen om de gebeurtenis &#39;interactie&#39; te activeren.

## Het rapport weergeven

- Aanmelden bij Journey Optimizer

- Ga naar Reisbeheer ->Campagnes

- Klik op de campagne en selecteer dan het aangewezen rapport van het rapportmenu.
