---
title: Pushkanaal maken
description: De configuratie van het drukkanaal bepaalt hoe de Web-dupberichten, met inbegrip van de toepassingsmontages en platform-specifieke details worden geleverd. Het koppelt ook uw pushinstellingen aan de vereiste referenties, zoals de VAPID-toetsen, zodat AJO meldingen kan verzenden naar geabonneerde gebruikers.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Pushkanaal maken

De eerste stap bestaat uit het maken van een pushkanaal in Adobe Journey Optimizer. Als onderdeel van deze instelling moet u VAPID-sleutels genereren die vereist zijn voor het verifiëren en inschakelen van webpushmeldingen. Deze sleutels worden dan gebruikt in de configuratie van het drukkanaal, die AJO toestaat om berichten aan geabonneerde gebruikers veilig te verzenden.

## VAPID-toetsen genereren

VAPID (vrijwillige serveridentificatie van de Toepassing) is een Web-push norm die uw server laat zich identificeren om de diensten (zoals Chrome, Edge, enz.) te duwen gebruikend openbare/privé zeer belangrijke paren, zodat weet de drukker wie het bericht verzendt.

Deze wordt gegenereerd met een hulpprogramma, zoals &#39;generate-vapid-keys&#39; voor het genereren van een openbare sleutel (gedeeld met de browser) en een persoonlijke sleutel (bewaard op de server) die samen wordt gebruikt voor het verifiëren en veilig verzenden van pushberichten.

Voor deze zelfstudie hebben we Node.js gebruikt om de VAPID-toetsen te genereren.

Controleer of Node.js is geïnstalleerd. Geef dan het volgende bevel uit
```npm install web-push -g ```

![&#x200B; web-push &#x200B;](assets/install-web-push.png)

```web-push generate-vapid-keys```

![&#x200B; vapid &#x200B;](assets/vapid-keys.png)

## Push Credential maken

* Aanmelden bij Journey Optimizer

* Navigeren naar Beheer | Kanalen | PUSH-INSTELLINGEN | Push Credentials| Push credential maken

* ![&#x200B; duw credential &#x200B;](assets/push-credential.png)

## Kanaalconfiguratie maken

* Aanmelden bij Journey Optimizer

* Navigeren naar Beheer | Kanalen | Kanaalconfiguratie maken
  ![&#x200B; kanaal-configuratie &#x200B;](assets/push-channel.png)
