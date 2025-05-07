---
title: Adobe Experience Platform-tags maken
description: AJO-soorten publiek maken op basis van de investeringsvoorkeuren van de gebruiker (voorraden, obligaties, cd's)
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17923
source-git-commit: 9695a4db0d0caa44a8c7d49e069320309ffc40a6
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---


# Adobe Experience Platform maken

Adobe Launch is geconfigureerd op de webpagina om de Adobe Experience Platform Web SDK te laden, zodat de sendEvent API-aanroep gepersonaliseerde ervaringen kan activeren. Deze opstelling zorgt ervoor dat de noodzakelijke cliënt-zijbibliotheken correct worden geïnitialiseerd, die interactie in real time met Adobe Journey Optimizer voor aanbiedingslevering toestaan.

* Aanmelden bij gegevensverzameling
* Klik op Labels -> Nieuwe eigenschap
* Maak een Adobe Experience Platform-tag met de naam ECID Service.

* De volgende extensies toevoegen aan de tag
  ![ markeringen-uitbreidingen ](assets/ecid-tag.png)

* Zorg ervoor dat u de Adobe Experience Platform Web SDK configureert voor het gebruik van de juiste omgeving en de DataStream voor financiële adviseurs die in de vorige zelfstudie is gemaakt
  ![ web-sdk-configuration ](assets/web-sdk-configuration.png)

* Er is geen aanvullende configuratie nodig voor Adobe Client Data Layer en Core-extensies

## Gegevenselement maken

Het ECID-gegevenselement in Adobe Launch wordt alleen gemaakt voor foutopsporing- en testdoeleinden. Hiermee kunnen ontwikkelaars de Experience Cloud-id weergeven die is toegewezen aan de browsersessie van een gebruiker. Zo kunnen identiteitsstitching worden gevalideerd en kunnen ze ervoor zorgen dat de sendEvent-aanroepen aan het juiste profiel zijn gekoppeld. Dit element wordt niet vereist voor personalisatie om te functioneren maar is nuttig tijdens implementatie en QA

![ ecid ](assets/ecid-data-element.png)


## AEP-tags opnemen op de HTML-pagina

Adobe Experience Platform-tags maken en publiceren

Wanneer een AEP-eigenschap Tags wordt gepubliceerd, geeft Adobe u een scripttag die u in uw HTML ``` <head>``` of onder aan de ``` <body>``` -tags moet plaatsen.

* Ga naar de eigenschap Tags (ECID Service).

* Klik op Milieu&#39;s en klik het installatiepictogram van het milieu u wilt (bijvoorbeeld, Ontwikkeling, het Staging, Productie).

* Noteer de ingesloten code. Deze code moet vlak voor de afsluitende tag ```</body>``` op de HTML-pagina worden geplaatst.

