---
title: De oplossing testen
description: Reis maken om e-mail te verzenden bij het verzenden van het formulier
feature: Journeys
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-12-25T00:00:00Z
jira: KT-20014
source-git-commit: 319b1cd4a037807a944e5fb6438e47b5fcf4c1c4
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# De oplossing testen


De oplossing testen
>[!VIDEO](https://video.tv.adobe.com/v/3478546)

## De voorbeeldelementen implementeren

Als u geïnstalleerde Node.js niet hebt, download en [&#x200B; installeer het van hier &#x200B;](https://nodejs.org/)

Installatie controleren door uit te voeren:

`node -v`

`npm -v`

## De projectmap instellen

Maak een nieuwe map voor de voorbeeldtoepassing met de volgende opdrachten:

`mkdir trigger-journey `

`cd trigger-journey`

## Het project initialiseren

`npm init -y`

## De vereiste frameworks installeren

`npm install express dotenv axios cors`

## Elementbestanden kopiëren

* Pak en plaats de inhoud van [&#x200B; project-root.zip &#x200B;](assets/project-root.zip) in de `trigger-journey` omslag uit.

* Maak een map met de naam `public` in de map `trigger-journey`
* Werk het `.env` -bestand bij met de juiste waarden. Deze waarden zijn beschikbaar via de gedownloade cURL-opdracht tijdens het maken van de HTTP Source-verbinding.
* Pak de inhoud van [&#x200B; index.zip &#x200B;](assets/index.zip) in de `public` omslag uit

## De server uitvoeren

Zorg ervoor dat u zich in de map `trigger-journey` bevindt.
De opdracht uitvoeren `node server.js`
Punt uw browser aan [&#x200B; Web-pagina &#x200B;](http://localhost:3000/)
Vul het formulier in en verzend het. De reis wordt in werking gesteld, en een e-mail wordt verzonden naar e-mailidentiteitskaart ingegaan in de vorm.


