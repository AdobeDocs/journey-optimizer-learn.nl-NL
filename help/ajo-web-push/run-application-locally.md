---
title: De toepassing lokaal uitvoeren
description: Stel de voorbeeldtoepassing lokaal in om de berichtstroom via webpushberichten te verkennen met AJO.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
exl-id: 2635641b-5ae2-4303-bac7-02c3702950f0
source-git-commit: c339fe796af1e691cd3b1c98cd6ba8a8772551e4
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# De toepassing lokaal uitvoeren

Deze pagina begeleidt u door de voorbeeldtoepassing lokaal in te stellen, zodat u de pushberichtstroom voor het web kunt testen en verkennen met Adobe Journey Optimizer. U kloont de opslagplaats, configureert omgevingsvariabelen en voert de toepassing uit op uw lokale systeem.


Voer de volgende stappen uit om de voorbeeldtoepassing op uw lokale systeem uit te voeren.

## 1. Install Node.js

Zorg ervoor u **Node.js (versie 16 of hoger)** geïnstalleerd op uw systeem hebt.

U kunt [&#x200B; het hier downloaden:](https://nodejs.org/)

De installatie controleren

```node -v```

```npm -v```


## &#x200B;2. Klonen in de opslagplaats

```git clone https://github.com/gbedekar489/ajo-web-push.git```

```cd ajo-web-push```

## &#x200B;3. Afhankelijkheden installeren

```npm install```

## &#x200B;4. Omgevingsvariabelen configureren

Maak een .env-bestand in de hoofdmap en voeg het volgende toe:

```
DATASTREAM_ID=your_datastream_id
ORG_ID=your_org_id
VAPID_PUBLIC_KEY=your_vapid_public_key
APP_ID=your_app_id
DATASET_ID=your_event_dataset_id
PORT=3000
```


Wanneer deze waarden lokaal worden uitgevoerd, worden deze gelezen uit het .env-bestand. In productie (b.v., geef terug), worden zij gevormd als milieuvariabelen.
