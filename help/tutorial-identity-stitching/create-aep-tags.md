---
title: CRMID naar Adobe Experience Platform verzenden
description: Adobe Experience Platform-tags maken om CRMID die u van de browser hebt ontvangen, naar Adobe Experience Platform te verzenden
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 894ad6b7-c4b4-465e-8535-3fdcd77e00eb
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 5%

---

# CRMID naar Adobe Experience Platform verzenden

Adobe Launch (Tags) wordt gebruikt om de CRMID naar Adobe Experience Platform (AEP) te verzenden, omdat deze een flexibel, gebeurtenisgestuurd mechanisme biedt voor het rechtstreeks verzenden van identiteitsgegevens vanuit de browser. Als u CRMID na gebruikersaanmelding verzendt, kan AEP de anonieme ECID koppelen aan het bekende CRM-profiel, zodat u een nauwkeurige identiteitscontrole kunt instellen. Deze koppeling vormt de basis voor het samenstellen van uniforme klantprofielen, het kwalificeren van doelgroepen en het aanbieden van persoonlijke realtime ervaringen in Adobe Journey Optimizer (AJO).

Er wordt een AEP-eigenschap met de naam FinWise gemaakt. De volgende extensies zijn toegevoegd aan de eigenschap Tags

![ markeringen-uitbreidingen ](assets/tags-extensions.png)

Configureer de AEP Web SDK-extensie met gebruik van de DataStream voor financiële adviseurs die in de vorige stap is gemaakt.
Experience Cloud ID Service is een optionele extensie die voor foutopsporingsdoeleinden aan de eigenschap tag wordt toegevoegd.

## Taggegevenselementen

De volgende gegevenselementen maken

| Gegevenselement | Extensie | Type gegevenselement | Aangepaste instellingen |
|--------------|-----------------------------------|---------------------------|----------------------------------------|
| crmid | Adobe Client Data Layer | Status Gegevenslaag berekend | user.crmid |
| ECID | Experience Cloud ID Service | ECID |                                        |
| identiteit | Adobe Experience Platform Web SDK | Identiteitskaart | ![afbeelding](assets/identity-settings.png) |
| XDMVariable | Adobe Experience Platform Web SDK | Variabele | ![afbeelding](assets/xdmvariable.png) |

## Regel maken

Maak een regel met de naam userLogin met de volgende gebeurtenis en handelingen

Gebeurtenis
![ gebeurtenis ](assets/data-pushed-event.png)

Variabele bijwerken, actie
![ update-veranderlijk ](assets/update-variable.png)
Gebeurtenisactie verzenden
![ send-event ](assets/send-event.png)

## Opslaan en samenstellen

Sla uw wijzigingen op, maak en maak de bibliotheek.
