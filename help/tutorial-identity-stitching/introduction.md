---
title: Naamplaatje in AEP
description: Identiteitsvervlechting tot stand brengen tussen een bekende gebruiker (CRMID) en een anonieme webbezoeker (ECID), toelatend verenigde profielen voor verpersoonlijking in real time en aanbiedersbesluit in Adobe Journey Optimizer (AJO).
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
exl-id: d6a1201a-3779-4718-8ea8-b88f925f53b6
source-git-commit: f3aeb66ca67448e7751ab2cd6d0bb6ce38f73530
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Identiteitsstitatie in AEP

In moderne klantervaringen is het essentieel om gebruikersidentiteiten te verenigen tussen apparaten en kanalen. Dit gebruiksgeval toont aan hoe te om identiteitsstitching in Adobe Experience Platform (AEP) uit te voeren door een bekende identiteitskaart van CRM-gevangen tijdens gebruikerslogin-met anonieme identiteitskaart van Experience Cloud (ECID) te verbinden die door SDK van het Web van Adobe wordt geproduceerd. Door deze identiteiten in real time samen te brengen, kan AEP een vollediger klantenprofiel bouwen dat zowel anoniem gedrag als voor authentiek verklaarde gegevens overspant. Dit maakt nauwkeuriger publiekssegmentatie, personalisatie en besluitvorming mogelijk binnen tools als Adobe Journey Optimizer (AJO).

## Vaardigheden vereist voor de zelfstudie Identiteitsplaatsing

Als u deze zelfstudie optimaal wilt benutten, is het raadzaam om vertrouwd te raken met het volgende:

- **de Concepten van de Kern van Adobe Experience Platform (AEP)**\
  Het begrip van schema&#39;s, datasets, identiteiten, fusiepolitiek, en real-time profielen.

- **Modellering van het Schema en van de Identiteit**\
  Mogelijkheid om identiteitsvelden te configureren in op profielen en gebeurtenissen gebaseerde schema&#39;s.

- **Adobe Lanceren (Markeringen) en Web SDK (Alloy.js)**\
  Ervaar met het instellen van Data Elements en Rules om gegevens naar AEP te verzenden via de Web SDK.

- **Basisbeginselen van JavaScript**\
  Comfortabel werken met functies om gebruikersinvoer, triggergebeurtenissen en foutopsporing van API-aanroepen vast te leggen.

- **AEP het Zuiveren Hulpmiddelen**\
  Mogelijkheid om de AEP Debugger en Identity Graph Viewer te gebruiken om identiteitsstitching te valideren.

- **Ingestie van Gegevens in AEP**\
  Kennis van het uploaden van steekproefgegevens naar datasets en het verzekeren van gegevenskwaliteit.


