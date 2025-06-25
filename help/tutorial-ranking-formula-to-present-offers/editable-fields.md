---
title: Bewerkbare formuliervelden gebruiken in AJO Code-gebaseerde ervaringen
description: Leer hoe u bewerkbare inhoudsblokken kunt maken met behulp van inlineformuliervelden in Adobe Journey Optimizer Code-Based Experience-sjablonen om marketers in staat te stellen dynamische, herbruikbare campagne-inhoud te maken.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-22T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18416
exl-id: 0ba695d6-becb-440d-b0d0-de5b51b42562
source-git-commit: 264dde0445306a6d75d8aa4e10459d02e34b2aa8
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---

# Bewerkbare formuliervelden gebruiken in AJO Code-gebaseerde ervaringen

Bij veel marketingreizen, met name in gereglementeerde industrieën, is het van essentieel belang om een juridische disclaimer op te nemen die kan variëren afhankelijk van de campagne, de geografie of het product. Door een [ editable gebied ](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/channels/code-based-experience-channel/form-fields-in-code-based-experiences) direct in de Redacteur van Personalization van AJO te gebruiken, kunnen de marketers en de juridische teams volledige controle over de ontkenningstekst handhaven zonder ontwikkelaars te impliceren of besluitvormingslogica te wijzigen.

Dit maakt snelle updates mogelijk en zorgt ervoor dat alle campagnes aan de vereisten voldoen en maakt gebruik van bepaalde inhoud, zoals aanbiedingen.

## Bewerkbaar veld invoegen in personalisatie-editor

- Open de campagne die u in de vorige stap hebt gemaakt.
- Klik _&#x200B;**wijzigen campagne**&#x200B;_
- Navigeer aan _&#x200B;**Inhoud**&#x200B;_ lusje
- Klik op _&#x200B;**geef code**&#x200B;_ uit en neem een editable gebied genoemd legalDisclaimer met een standaardwaarde op gebruikend de volgende syntaxis in de verpersoonlijkingsredacteur

- &#x200B;
  <pre><code>&#123;&#123;#inline &quot;legalDisclaimer&quot; name=&quot;Legal Disclaimer&quot;&#125;&#125; Legal Disclaimer will go here &#123;&#123;/inline&#125;&#125;</code></pre>

- <code> {{legalDisclaimer}} gebruiken</code> variabele in de template, zoals hieronder weergegeven

- ![ editable-fields ](assets/editable-fields.png)

- Marketers kunnen het veld Legal Disclaimer eenvoudig bewerken zonder de personalization editor te hoeven openen.
- ![ editable-field-marketer ](assets/editable-field-marketer-view.png)



## De campagne publiceren

Activeer de campagne om persoonlijke aanbiedingen in real-time te leveren.
