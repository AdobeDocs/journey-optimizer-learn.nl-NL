---
title: Gebruikersrepresentatie vastleggen
description: Maak een webpagina om vast te leggen dat de gebruiker ermee instemt pushberichten te ontvangen.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Gebruikersrepresentatie vastleggen

Op deze webpagina wordt vastgelegd of de gebruiker toestemming heeft gegeven om pushberichten te ontvangen. De gebruiker wordt gevraagd om meldingen in te schakelen met behulp van de browser Notifications API en bij acceptatie wordt het push-abonnement geregistreerd bij Adobe Experience Platform met behulp van de Web SDK. Dit zorgt ervoor dat alleen gebruikers met de keuze in aanmerking komen voor pushberichten via campagnes en reizen in Adobe Journey Optimizer.

Als u pushmeldingen via het web wilt inschakelen, laadt de pagina eerst een configuratiebestand door fetch(&quot;/config&quot;) binnen een initialisatiefunctie aan te roepen. Deze configuratie wordt bediend door een toepassing Node.js en omvat zeer belangrijke waarden zoals gegevensstroom identiteitskaart, organisatie identiteitskaart, VAPID openbare sleutel, toepassings identiteitskaart, en het volgen dataset identiteitskaart Zodra de configuratie wordt geladen, wordt het Web SDK van Adobe geïnitialiseerd en de de dienstarbeider wordt geregistreerd om pushoverseinen te steunen. Wanneer een gebruiker op Meldingen inschakelen klikt, vraagt de browser de gebruiker om toestemming met behulp van de API voor webmeldingen. Als de toestemming wordt verleend, verzendt het Web SDK het pushabonnement naar Adobe Experience Platform, en de gebruiker wordt duidelijk zoals binnen binnen binnen 24 uur verkiest om herhaalde herinneringen te vermijden. U kunt deze stroom op het lokale Web-pagina shop-smart.html proberen inbegrepen in de [ steekproeftoepassing ](http://localhost:3000/) na de aanvang van de server.

![ verzoek-toestemmingen ](assets/request-notifications.png)

