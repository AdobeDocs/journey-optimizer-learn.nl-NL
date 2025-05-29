---
title: Willekeurige formule maken
description: Bij het nemen van de biedingen wordt in Adobe Journey Optimizer een rangschikkingsformule gebruikt, met name in het kader van een selectiestrategie om de prioriteitsvolgorde van de in aanmerking komende aanbiedingen te bepalen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
jira: KT-18188
source-git-commit: 58d2964644bc199b9db212040676d87d54f767b9
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---


# Willekeurige formule maken

Bij het nemen van de biedingen wordt in Adobe Journey Optimizer een rangschikkingsformule gebruikt, met name in het kader van een selectiestrategie om de prioriteitsvolgorde van de in aanmerking komende aanbiedingen te bepalen. De rangschikkingsformule wordt toegepast na het filteren van de geschiktheid, wanneer meerdere aanbiedingen in aanmerking komen voor een bepaald profiel, maar alleen de bovenste (of weinige) aanbiedingen moeten worden gepresenteerd op basis van bedrijfslogica of profielcontext.

* Aanmelden bij Journey Optimizer

* Beslissing ->Strategie-instelling ->Beoordelingsformules ->Formule maken

Willekeurige formule
![ name_description ](assets/formuala-ranking.png)

Een criterium in een rangschikkingsformule verwijst naar een voorwaardelijke regel die wordt gebruikt om een score aan een aanbieding toe te wijzen. Deze criteria vergelijken de kenmerken van de aanbieding en het profiel of de context om te bepalen hoe relevant een aanbieding voor een specifieke persoon is.



Criteria 1
![ criteria_one ](assets/criteria1.png)

Criteria 1 bevatten drie criteria:

* voorstel._techmarketingdemos.aanbiedingDetails.zipCode == &quot;92128&quot; - controleert de postcode verbonden aan de aanbieding.

* _techmarketingdemos.zipCode == &quot;92128&quot; - hiermee wordt de ZIP-code op het profiel van de gebruiker gecontroleerd.

* _techmarketing demos.yearIncome > 100000 - controleert het inkomensniveau van het profiel van de gebruiker.

Als aan al deze criteria wordt voldaan, krijgt de aanbieding een score van 40.






Criteria 2
![ criteria_two ](assets/criteria2.png)

Criteria 2 bevatten drie criteria:

* voorstel._techmarketingdemos.aanbiedingDetails.zipCode == &quot;92126&quot; - controleert de postcode verbonden aan de aanbieding.

* _techmarketingdemos.zipCode == &quot;92126&quot; - hiermee wordt de ZIP-code op het profiel van de gebruiker gecontroleerd.

* _techmarketing demos.yearIncome &lt; 100000 - controleert het inkomensniveau van het profiel van de gebruiker.

Als aan al deze criteria wordt voldaan, krijgt de aanbieding een score van 30.




