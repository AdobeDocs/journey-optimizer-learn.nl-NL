---
title: Beslissingsbeleid maken
description: Een besluitvormingsbeleid bepaalt de logica die wordt gebruikt om te bepalen welke aanbiedingen aan een gebruiker tijdens verpersoonlijking worden geleverd.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 186e4a7d-6077-401f-9958-2f955214bc35
source-git-commit: 6bf0c2487afff4811aa94e9591ae29c38af15d34
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Beslissingsbeleid maken

Beslissingsbeleid zijn containers voor uw aanbiedingen die de beslissingsengine gebruiken om de beste inhoud te kiezen die u kunt leveren, afhankelijk van het publiek.

In de verpersoonlijkingsredacteur, klik op het beleidspunt van het Besluit in de linkernavigatie en klik dan op Add besluitvormingsbeleid

![ creeer-besluit-beleid ](assets/decision-policy.png)

Klik op Toevoegen om de selectiestrategie te selecteren
Klik op Back-up selecteren om het voorstel voor terugvallen te selecteren.
Klik op Volgende om het beslissingsbeleid te bekijken en klik op Maken om het proces voor het maken van het beslissingsbeleid te voltooien.


![ besluit-beleid ](assets/decision-policy2.png)


## Het beslissingsbeleid in de code-editor gebruiken

Van de verpersoonlijkingsredacteur, klik op het beleid van het Tussenvoegsel.De code die aan het besluitbeleid beantwoordt wordt toegevoegd.

In dit stadium kunt u alle vereiste beslissingskenmerken rechtstreeks in de code opnemen. Deze kenmerken worden gedefinieerd in het schema dat wordt gebruikt in de catalogus met aanbiedingen. Standaardkenmerken worden geordend onder de naamruimte __experience, terwijl aangepaste kenmerken die specifiek zijn voor uw organisatie, worden opgeslagen onder de naamruimte `_<imsOrg>` .

![ using_decisions_polcy ](assets/Insert-policy.png)

Deze code doorloopt een lijst met persoonlijke aanbiedingen die voor de gebruiker zijn gekozen en geeft de tekst voor elke aanbieding op de webpagina weer. Het toont het bericht (genoemd offerText) van elk aanbod binnen een paragraaf, zodat kunnen de gebruikers hun op maat gemaakte inhoud duidelijk zien.
Als geen gepersonaliseerde aanbieding beschikbaar is, een fallback aanbieding-wordt getoond om ervoor te zorgen de ruimte niet leeg wordt verlaten.

Klik op Opslaan en activeer de campagne.
