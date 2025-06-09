---
title: Willekeurige formule maken
description: Bij het nemen van de biedingen wordt in Adobe Journey Optimizer een rangschikkingsformule gebruikt, met name in het kader van een selectiestrategie om de prioriteitsvolgorde van de in aanmerking komende aanbiedingen te bepalen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-10T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18258
source-git-commit: d46c5a922b8448f57b8a730188284294c3caba96
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Willekeurige formule maken

Bij het nemen van de biedingen wordt in Adobe Journey Optimizer een rangschikkingsformule gebruikt, met name in het kader van een selectiestrategie om de prioriteitsvolgorde van de in aanmerking komende aanbiedingen te bepalen. De rangschikkingsformule wordt toegepast na het filteren van de geschiktheid, wanneer meerdere aanbiedingen in aanmerking komen voor een bepaald profiel, maar alleen de bovenste (of weinige) aanbiedingen moeten worden gepresenteerd op basis van bedrijfslogica of profielcontext.

* Aanmelden bij Journey Optimizer

* Beslissing ->Strategie-instelling ->Beoordelingsformules ->Formule maken

Noem de formule _&#x200B;**Weer - Verwant - Aanbiedingen**&#x200B;_



Een criterium in een rangschikkingsformule verwijst naar een voorwaardelijke regel die wordt gebruikt om een score aan een aanbieding toe te wijzen. Deze criteria vergelijken de kenmerken van de aanbieding en de context om te bepalen hoe relevant een aanbieding voor een specifieke persoon is.

De volgende 3 criteria worden gedefinieerd om aanbiedingen te filteren en dan een rangschikkingsscore toe te wijzen aan de kwalificerende aanbieding. De criteria worden gedefinieerd met behulp van de criteria builder. De contextgegevens kunnen ook worden gebruikt voor het definiëren van de criteria zoals weergegeven in de onderstaande schermafbeelding
![ context-gegevens ](assets/context-data.png)

Alle drie de criteria hebben bij het definiëren van de criteria een aanbiedingskenmerk(tag) en een kenmerk(temperatuur) voor contextgegevens gebruikt.

## Criteria één

| **de Markering van de Aanbieding** | **de gegevensvoorwaarde van de context** | **Logica van de Score** |
|------------------|---------------------|-------------------------------------|
| **heet** | temperatuur > 80 | score=Temperatuur |


## Criteria twee

| **Markering van het Weer** | **de gegevensvoorwaarde van de context** | **Logica van de Score** |
|------------------|---------------------------|----------------------------------------------|
| **lente** | temperatuur > 65 en &lt; 80 | score=temperatuur × 4 |

## Criteria drie

| **Markering van het Weer** | **de gegevensvoorwaarde van de context** | **Logica van de Score** |
|------------------|---------------------------|----------------------------------------------|
| **koud** | temperatuur &lt; 65 | score = temperatuur |
