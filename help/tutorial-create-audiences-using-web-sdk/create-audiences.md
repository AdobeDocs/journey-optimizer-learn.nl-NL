---
title: Soorten publiek maken in Adobe Journey Optimizer
description: Leer hoe u een doelgericht publiek in AJO kunt definiëren en opbouwen voor persoonlijke klantritten en realtime beslissingen
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
jira: KT-17923
source-git-commit: ba83be3caf214d2daaa8c99556d246686ff3f0cb
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Soorten publiek maken in Adobe Journey Optimizer


Soorten publiek in Adobe Experience Platform zijn groepen gebruikers die zijn gemaakt op basis van hun handelingen, voorkeuren of profielgegevens voor persoonlijke ervaringen.

* Aanmelden bij Journey Optimizer
* Ga naar Klant -> Soorten publiek ->Haakje maken
* Creeer Publiek gebruikend de methode van de Regel van de Bouwstijl

  ![ publiek ](assets/rule-based-audience.png)

* De volgende 3 soorten publiek maken

   * Klanten die geïnteresseerd zijn in voorraden

   * Klanten die geïnteresseerd zijn in obligaties

   * Klanten die geïnteresseerd zijn in cd


* Zorg ervoor dat de evaluatiemethode voor elk publiek aan _**Edge**_ voor kwalificatie in real time wordt geplaatst.
  ![ rand-publiek ](assets/audience-edge.png)

* Gebruik het veld PreferredFinancialInstrument om gebruikers te segmenteren op basis van hun geselecteerde investeringsrente, zoals voorraden, obligaties of cd&#39;s

![ gebeurtenis ](assets/event-attribute.png)

![ PreferredFinancialInstrument ](assets/stock-customers.png)




>[!NOTE]
>
>>Als het veld PreferredFinancialInstrument niet zichtbaar is op het tabblad Gebeurtenissen, klikt u op het pictogram Instellingen en schakelt u het volledige XDM-schema tonen in of uit.



![ knevel-volledig-xdm-schema ](assets/show-custom-fields.png)


