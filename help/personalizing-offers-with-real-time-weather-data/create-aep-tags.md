---
title: Adobe Experience Platform-tags maken
description: AJO-soorten publiek maken op basis van de investeringsvoorkeuren van de gebruiker (voorraden, obligaties, cd's)
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
exl-id: 04fad076-e897-4831-9147-768721858a80
source-git-commit: 40690024e5348dd3ac05f350e49a67a99d5e455e
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Adobe Experience Platform-tags maken

Met Adobe Experience Platform Tags (voorheen Adobe Launch) kunt u marketing- en analysetechnologieën* op uw website beheren en implementeren zonder dat u de code van de site hoeft te wijzigen.

Deze [ video beschrijft het proces om de Markeringen van de Ervaring van Adobe te creëren ](https://experienceleague.adobe.com/en/playlists/experience-platform-get-started-with-tags)

- Aanmelden bij gegevensverzameling
- Klik op _&#x200B;**Markeringen -> Nieuw Bezit**&#x200B;_

- Creeer een markering van Adobe Experience Platform genoemd _&#x200B;**verpersoonlijking-op-weer**&#x200B;_.

- De volgende extensies toevoegen aan de tag
  ![ markeringen-uitbreidingen ](assets/tags-extensions1.png)
- Voeg een gegevenselement met de naam ECID toe, zoals hieronder wordt weergegeven. Dit gegevenselement wordt later gebruikt bij de rapportage
  ![ ecid-data-element ](assets/ecid-data-element.png)

- Zorg ervoor om het Web SDK van Adobe Experience Platform te vormen om het correcte milieu en **weer-verwant-datastream** te gebruiken die in de vroegere stap wordt gecreeerd.
  ![ web-sdk-configuration ](assets/tags-extensions.png)



## AEP-tags maken en implementeren


Maak een nieuwe bibliotheek en voeg alle gewijzigde bronnen aan de bibliotheek toe, zoals geïllustreerd in de onderstaande schermafbeeldingen.

**voeg bibliotheek** toe

![ nieuw-bibliotheek ](assets/tag-add-library.png)

**creeer een bibliotheek**

Geef in het scherm Bibliotheek maken de naam van de bibliotheek en de omgeving op.

Alle gewijzigde bronnen toevoegen aan deze bibliotheek
![ markering-bibliotheek ](assets/tag-build-library.png)

Klik vervolgens op de knop Opslaan en bouwen naar ontwikkeling om de bibliotheek te maken

## AEP-tags opnemen op de HTML-pagina

Wanneer u een AEP-eigenschap Tags publiceert, geeft Adobe u een scripttag die u in de HTML ``` <head>``` -tags of onder aan de ``` <body>``` -tags moet plaatsen.

- Ga naar de eigenschap Tags (personalization-on-weer).

- Klik op Milieu&#39;s en klik het installatiepictogram van het milieu u wilt (bijvoorbeeld, Ontwikkeling, het Staging, Productie).

- Noteer de ingesloten code. Dit is nodig in een later stadium van deze zelfstudie.
