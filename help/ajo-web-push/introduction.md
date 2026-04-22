---
title: Web push in AJO
description: Deze zelfstudie laat zien hoe u pushmeldingen via het web kunt implementeren met Adobe Journey Optimizer (AJO). U zult leren hoe te om gebruikersopt-in met het Web SDK te vangen, berichten door geplande campagnes te verzenden, en dupberichten in real time teweeg te brengen gebruikend een douane price.drop gebeurtenis met de Markeringen van AEP.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Web push in Adobe Journey Optimizer

Pushmeldingen via het web zijn een krachtige manier om gebruikers opnieuw in real-time te laten deelnemen. Deze zelfstudie begeleidt u door het implementeren van gebruikers met Adobe Journey Optimizer (AJO). U begint met het gebruik van de Web SDK om de gebruikersvoorkeur voor pushberichten vast te leggen, zodat u een naadloze en compatibele abonnementservaring hebt. Vervolgens maakt u een campagne om pushmeldingen te verzenden naar gebruikers die zich hebben aangemeld, zodat ze betrokkenheid van het publiek mogelijk maken. Tot slot leert u hoe u AEP-tags kunt gebruiken om een gebeurtenis voor het neerzetten van een aangepaste prijs te activeren. Deze gebeurtenis start een reis in AJO en biedt tijdige, persoonlijke pushberichten op basis van real-time gebruikersgedrag.

Voorbeeld van een webpagina waarmee gebruikers zich kunnen aanmelden voor meldingen

![ toe:laten-berichten ](assets/enable-notifications.png)

Voorbeeld van een webpagina die de gebeurtenis price drop activeert

![ daling van de trekkerprijs ](assets/trigger-price-drop-event.png)

## Vereisten

Deze zelfstudie is ontworpen om in de praktijk te worden uitgevoerd en eenvoudig te worden opgevolgd. Hoewel er geen grondige expertise vereist is, is het nuttig om de volgende concepten als basiskennis te nemen:

- Adobe Journey Optimizer (reizen of campagnes maken)
- AEP-gegevensverzameling (tags) en de Web SDK
- Standaard Adobe Experience Platform-concepten zoals schema&#39;s en gebeurtenissen
- Sommige JavaScript- en algemene concepten voor webontwikkeling
- De basis kennis Node.js (voor het produceren van sleutels VAPID en het dienen van een eenvoudig config eindpunt)

Als u aan om het even welk van deze gebieden nieuw bent, maak u geen zorgen-het leerprogramma zal u door de belangrijkste stappen onderweg begeleiden.
Deze zelfstudie richt zich op de implementatie van een gebruiksscenario voor pushmeldingen van begin tot eind, zodat u op effectieve wijze kunt volgen op basis van de praktische kennis van de bovenstaande gereedschappen en concepten.


## 🔔 Browsermeldingen inschakelen

Als meldingen zijn geblokkeerd of niet worden weergegeven, moet u deze mogelijk inschakelen in de browserinstellingen. Raadpleeg de onderstaande hulplijnen:

- **Google Chrome (Vensters/macOS)**\
  <https://support.google.com/chrome/answer/3220216>

- **Microsoft Edge (Vensters)**\
  <https://support.microsoft.com/en-us/microsoft-edge/manage-website-notifications-in-microsoft-edge>

- **Safari (macOS)**\
  <https://support.apple.com/guide/safari/customize-website-notifications-sfri40734/mac>

- **Safari (iPhone/iPad)**\
  <https://support.apple.com/en-us/HT213893>


## Voorbeeldtoepassing


Er is een complete voorbeeldtoepassing beschikbaar om u te helpen de stappen te volgen.

- [ Levende Demo - Opt-in:](https://ajo-web-push.onrender.com/)

- [ de Daling van de Prijs van de trekker Gebeurtenis:](https://ajo-web-push.onrender.com/price-drop-trigger.html)

- [ Code van Source:](https://github.com/gbedekar489/ajo-web-push)

U kunt de live demo verkennen om de flow in actie te zien of de repository te klonen om het project lokaal uit te voeren.

