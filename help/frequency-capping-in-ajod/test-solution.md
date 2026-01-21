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
exl-id: 6b6c66d3-218d-4f5b-adb0-a2eca05989ab
source-git-commit: bef6d831c639d40514552dae3ff20132626a4a09
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# De oplossing testen

## De voorbeeldelementen implementeren

Als u geïnstalleerde Node.js niet hebt, download en [&#x200B; installeer het van hier &#x200B;](https://nodejs.org/)

Installatie controleren door uit te voeren:

`node -v`

`npm -v`

## De projectmap instellen

Maak een nieuwe map voor de voorbeeldtoepassing met de volgende opdrachten:

`mkdir frequency-capping `

`cd frequency-capping `

## Het project initialiseren

`npm init -y`

## De vereiste frameworks installeren

`npm install express`

## Elementbestanden kopiëren

* Pak en plaats de inhoud van [&#x200B; server.zip &#x200B;](assets/server.zip) in de `frequency-capping` omslag uit.
* Extraheer de inhoud van [&#x200B; public.zip &#x200B;](assets/public.zip) in de &quot;frequentie-capping&quot;omslag

## De URL van het oppervlak in het JavaScript-bestand bijwerken

Open `frequency-capping.js` in `public\scripts` en werk de eigenschap surfaces bij zodat deze overeenkomt met de kanaalconfiguratie die in de campagne wordt gebruikt

## JS-server voor knooppunt starten

Ga naar de map `c:\frequency-capping` . Voer het bevel `node server.js` uit om de knoopJs server op haven 3000 te beginnen


## De eigenschap Adobe Experience Platform-tags bijwerken

Open het bestand `frequency-capping.html` in de map `public` in de teksteditor en vervang de scripttag door de scripttag van de Adobe Experience Platform-tageigenschap die u in de vorige stap van deze zelfstudie hebt gemaakt. Sla het bestand op

```
<script src="https://assets.adobedtm.com/AEM_TAGS/launch-ENabcd1234.min.js" async></script>
```

## Interactie met de aanbiedingen

* Open [&#x200B; webpage &#x200B;](http://localhost:3000) in uw favoriete browser.
* Interactie met de aanbieding
* De pagina vernieuwen
* Afhankelijk van de regels voor het aftopping van de frequentie, moet u een nieuwe aanbieding zien

## Het rapport weergeven

* Aanmelden bij Journey Optimizer
* Ga naar Reisbeheer ->Campagnes
* Klik op de campagne en selecteer dan het aangewezen rapport van het rapportmenu.
