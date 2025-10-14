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
source-git-commit: 667f146639635515a5572e9ace41d83ab4452bb8
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 5%

---

# CRMID naar Adobe Experience Platform verzenden

Adobe Experience Platform-tags worden gebruikt om de CRMID naar Adobe Experience Platform (AEP) te verzenden, omdat deze een flexibel, gebeurtenisgestuurd mechanisme biedt voor het rechtstreeks verzenden van identiteitsgegevens vanuit de browser. Als u CRMID na gebruikersaanmelding verzendt, kan AEP de anonieme ECID koppelen aan het bekende CRM-profiel, zodat u een nauwkeurige identiteitscontrole kunt instellen. Deze koppeling vormt de basis voor het samenstellen van uniforme klantprofielen, het kwalificeren van doelgroepen en het aanbieden van persoonlijke realtime ervaringen in Adobe Journey Optimizer (AJO).

Een bezit van de Markeringen van Experience Platform genoemd _&#x200B;**FinWise**&#x200B;_ wordt gecreeerd. De volgende extensies zijn toegevoegd aan de eigenschap Tags

![&#x200B; markeringen-uitbreidingen &#x200B;](assets/tags-extensions.png)

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

Maak een regel met de naam LoginEvent met de volgende gebeurtenis en handelingen

Gebeurtenis
![&#x200B; gebeurtenis &#x200B;](assets/data-pushed-event1.png)

Variabele bijwerken, actie
![&#x200B; update-veranderlijk &#x200B;](assets/update-variable1.png)
Gebeurtenisactie verzenden
![&#x200B; send-event &#x200B;](assets/send-event1.png)

## Opslaan en samenstellen

Sla uw wijzigingen op, maak en maak de bibliotheek.
