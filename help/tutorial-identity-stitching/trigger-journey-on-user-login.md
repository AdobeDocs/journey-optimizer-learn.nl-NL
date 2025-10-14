---
title: Adobe Journey Optimizer Journey activeren met Adobe Web SDK
description: Leer een reis van Adobe Journey Optimizer van plaatsgebeurtenissen zoals gebruikerslogin te beginnen door het Web SDK van AEP te gebruiken dat door de Markeringen van Adobe Experience Platform wordt gevormd
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-09-24T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-19287
source-git-commit: 6927cade07790603e711f4e6e4c3f6982a56e6f5
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Adobe Journey Optimizer Journey activeren met Adobe Web SDK

In deze extensie van de zelfstudie Identiteitsbeheer wordt een Adobe Journey Optimizer-reis gestart die de aangemelde gebruiker via zijn ingesloten profiel per e-mail verzendt. **Dit artikel veronderstelt u met het e-mailkanaal vertrouwd bent en inhoud voor het e-mailkanaal creeert.**

## Configuratie van e-mailkanalen maken

* Login aan _**Journey Optimizer**_
* Navigeer aan _**Beleid -> Kanalen -> creeer kanaalconfiguratie**_
* Selecteer **E-mail** van de kanaallijst. Geef een relevante naam en beschrijving op.
* Vul de e-mailinstellingen in.
* Geef de details van de uitvoering op zoals hieronder wordt weergegeven. De e-mail wordt verzonden naar het e-mailadres van het profiel dat is opgeslagen in het veld
* ![ e-mail-kanaal ](assets/email-channel-execution.png)
* De configuratie van het e-mailkanaal activeren

## Gebeurtenis maken

* Login aan _**Journey Optimizer**_
* Navigeer aan _**Beleid -> Configuraties**_
* Klik op de knop Beheren van de gebeurtenissenkaart en klik op Gebeurtenis maken. Geef de hieronder weergegeven waarden op
* ![ reis-gebeurtenis ](assets/journey-event1.png)

* Controleer of het eventType van de gebeurtenis gelijk is aan LoginEvent. Het type `LoginEvent` wordt ingesteld in de Adobe Experience Platform-tag.
* De gebeurtenis opslaan

## Reis maken

* Login aan _**Journey Optimizer**_
* Navigeer aan _**Beheer van de Reis -> Reizen -> creeer Reis**_
* Sleep en laat vallen de _**UserLoggedIn**_ gebeurtenis op het canvas
* Sleep E-mail vanuit het menu Handelingen. Configureer de e-mailactie om de configuratie van het e-mailkanaal te gebruiken die u eerder hebt gemaakt.
* Publiceer de reis.

## Hoe de reis wordt geactiveerd

De reis wordt teweeggebracht wanneer de gebeurtenislading die via het Web SDK wordt verzonden, aanpast wat in de reis wordt gevormd. In dit voorbeeld is het gebeurtenistype `UserLoggedIn` `LoginEvent` .

* Dit controleren door het reisrapport te bekijken
* ![ reis-rapport ](assets/journey-triggered-report.png)




