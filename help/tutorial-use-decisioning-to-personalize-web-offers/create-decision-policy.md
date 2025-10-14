---
title: Een beslissingsbeleid maken
description: Gebruik een besluitvormingsbeleid om de logica te bepalen die aanbiedingen aan een gebruiker tijdens verpersoonlijking worden geleverd.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-17728
exl-id: 186e4a7d-6077-401f-9958-2f955214bc35
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# Beslissingsbeleid maken

Het beleid van het besluit is containers voor uw aanbiedingen die hefboomwerking de [!UICONTROL &#x200B; Duidelijke &#x200B;] motor om de beste inhoud te kiezen te leveren, afhankelijk van het publiek.

1. In de verpersoonlijkingsredacteur, klik **punt van het beleid van de Beslissing** in de linkernavigatie, dan klik **[!UICONTROL besluitvormingsbeleid]** toevoegen.

   ![&#x200B; creeer-besluit-beleid &#x200B;](assets/decision-policy.png)

1. Klik **[!UICONTROL toevoegen]** om de selectiestrategie te selecteren.

   ![&#x200B; besluit-beleid &#x200B;](assets/decision-policy2.png)

1. Klik **[!UICONTROL Uitgezochte reserve]** om de herfstaanbieding te selecteren.
1. Klik **[!UICONTROL daarna]** om het besluitvormingsbeleid te herzien.
1. Klik **[!UICONTROL creëren]** om het proces te voltooien om het besluitvormingsbeleid tot stand te brengen.

## Het beslissingsbeleid in de code-editor gebruiken

1. Van de verpersoonlijkingsredacteur, klik **[!UICONTROL beleid van het Tussenvoegsel]**.

   De code die overeenkomt met het beslissingsbeleid wordt toegevoegd.

   In dit stadium kunt u alle vereiste beslissingskenmerken rechtstreeks in de code opnemen. Deze kenmerken worden gedefinieerd in het schema dat wordt gebruikt in de catalogus met aanbiedingen. Standaardkenmerken worden geordend onder de naamruimte `__experience` , terwijl aangepaste kenmerken die specifiek zijn voor uw organisatie worden opgeslagen onder de naamruimte `_<imsOrg>` .

   ![&#x200B; using_decisions_polcy &#x200B;](assets/Insert-policy.png)

   Deze code doorloopt een lijst met persoonlijke aanbiedingen die voor de gebruiker zijn gekozen en geeft de tekst voor elke aanbieding op de webpagina weer. Het toont het bericht (genoemd `offerText`) van elke aanbieding binnen een paragraaf, zodat kunnen de gebruikers hun op maat gemaakte inhoud duidelijk zien.

   Als er geen persoonlijke aanbieding beschikbaar is, wordt een fallback-aanbieding weergegeven om ervoor te zorgen dat de ruimte niet leeg blijft.

1. Klik **[!UICONTROL sparen]**, dan activeer de campagne.
