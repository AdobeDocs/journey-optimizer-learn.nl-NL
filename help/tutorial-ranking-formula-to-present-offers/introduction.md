---
title: Aanbiedingen personaliseren met rangschikkende formules op basis van postcode en inkomen
description: Gebruik Adobe Journey Optimizer-rangschikkingsformules om dynamisch de meest relevante financiële aanbiedingen te bedienen, op maat van de ZIP-code en het inkomensniveau van elke gebruiker, voor een betere betrokkenheid en slimmere personalisatie.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-27T00:00:00Z
jira: KT-18188
exl-id: 11685f7c-8048-4318-9c28-71bd7da8f7ff
source-git-commit: 85d3def3afb1d073b133df40e4cbf32d00a3a5c9
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# Aanbiedingen personaliseren met rangschikkingsformules op basis van zip-code van gebruikers en inkomen

Dit gebruiksscenario laat zien hoe u persoonlijke financiële aanbiedingen kunt aanbieden door gebruikerskenmerken zoals postcode en jaarinkomen in Adobe Journey Optimizer te benutten. Door rangschikkingsformules te gebruiken, worden aanbiedingen intelligent gescoord en geprioriteerd gebaseerd op locatiespecifieke promoties en op inkomen-gebaseerde subsidiabiliteit. Zo kunnen cd&#39;s met een hoog rendement bijvoorbeeld worden bevorderd tot gebruikers in welvarende ZIP-codes, terwijl aan opkomende investeerders verschillende investeringsopties worden getoond. De rangschikkingsformules zorgen ervoor dat elke gebruiker aanbiedingen ontvangt die zowel relevant als financieel passend zijn. De rangschikkingscriteria worden bepaald gebruikend profielattributen, contextuele signalen, en facultatieve AI modellen om besluitprecisie verder te verbeteren. Aanbiedingen worden in real-time geleverd via internet of e-mail, wat leidt tot een hogere betrokkenheid en conversie. Deze benadering combineert bedrijfslogica met gegeven-gedreven verpersoonlijking om de gebruikerservaring en marketing effect te verhogen.

## Vereisten

Deze zelfstudie bouwt verder op de belangrijkste Adobe Journey Optimizer- en Adobe Experience Platform-concepten. Controleer voordat u verdergaat of aan de volgende voorwaarden is voldaan:

* [ het Zelfstudie van het Stitching van de Identiteit ](https://experienceleague.adobe.com/nl/docs/journey-optimizer-learn/tutorial-on-identity-stitching-in-aep/introduction) is voltooid, met CRM IDs met succes verbonden aan ECIDs in Adobe Experience Platform.

* Begrijp met het creëren van Punten van de Aanbieding in AJO, met inbegrip van inhoudsdefinitie, meta-gegevensopstelling, en geschiktheidsregels.

* Kennis van het configureren van kanalen (zoals Web of E-mail) voor levering van aanbiedingen.

* Kennis van het maken en activeren van campagnes in AJO.

* Begrijp met het gebruiken van de Lancering van Adobe (Markeringen) om het Web SDK op te stellen en gebeurtenissen te verzenden die identiteit en profielgegevens bevatten.

In deze zelfstudie worden de volgende stappen in de besluitvorming over aanbiedingen besproken:

* Een beoordelingsmethode maken met behulp van profielkenmerken zoals postcode en jaarinkomen.

* Het bepalen van een Strategie van de Selectie om aanbiedingen te groeperen en voorrang te geven.

* Opzetten van een besluitvormingsbeleid om elk individu het meest relevante aanbod te bieden.
