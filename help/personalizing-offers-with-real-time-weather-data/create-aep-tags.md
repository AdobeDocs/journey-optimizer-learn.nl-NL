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
source-git-commit: dac6b373226bd0be2533cf859e4f250018cf568b
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# AEP-tags maken

Met Adobe Experience Platform Tags (voorheen Adobe Launch) kunt u marketing- en analysetechnologieën* op uw website beheren en implementeren zonder dat u de code van de site hoeft te wijzigen.

Deze [ video beschrijft het proces om de Markeringen van de Ervaring van Adobe te creëren ](https://experienceleague.adobe.com/nl/playlists/experience-platform-get-started-with-tags)

* Aanmelden bij gegevensverzameling
* Klik op Labels -> Nieuwe eigenschap
* Creeer een markering van Adobe Experience Platform genoemd _&#x200B;**verpersoonlijking-op-weer**&#x200B;_.

* De volgende extensies toevoegen aan de tag
  ![ markeringen-uitbreidingen ](assets/tags-extensions1.png)

* Zorg ervoor om het Web SDK van Adobe Experience Platform te vormen om het correcte milieu en **weer-verwant-datastream** te gebruiken die in de vroegere stap wordt gecreeerd.
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

* Ga naar de eigenschap Tags (personalization-on-weer).

* Klik op Milieu&#39;s en klik het installatiepictogram van het milieu u wilt (bijvoorbeeld, Ontwikkeling, het Staging, Productie).

* Noteer de ingesloten code. Dit is nodig in een later stadium van deze zelfstudie.
