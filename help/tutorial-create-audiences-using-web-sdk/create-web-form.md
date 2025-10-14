---
title: Een webformulier maken
description: Een formulier op uw HTML-pagina maken waarmee gebruikers hun investeringsvoorkeur kunnen selecteren
feature: Audiences
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-04-30T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-17923
exl-id: 20de8dec-aac8-43ed-8305-e723f82a5dd9
source-git-commit: 163edfb3367d03729d68c9339ee2af4a0fe3a1b3
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Een webformulier maken

Het volgende HTML-formulier is gemaakt om de gebruikersvoorkeur vast te leggen
![&#x200B; html-vorm &#x200B;](assets/web-form.png)

Wanneer een gebruiker op de knop op de webpagina klikt, wordt de geselecteerde financiële voorkeur (zoals Standen, Obligaties of Cd&#39;s) vastgelegd en in de gegevenslaag van Adobe geplaatst. Met deze gebeurtenis (assetClassSelection) wordt de keuze van de gebruiker in real-time opgeslagen. Adobe Launch luistert vervolgens naar deze gebeurtenis, haalt de geselecteerde investeringsoptie (PreferredFinancialInstrument) op en kan acties activeren zoals het verzenden van de gegevens naar Adobe Experience Platform (AEP) of het bijwerken van de personalisatieregels

De volgende JavaScript is geschreven om het verzenden van het formulier af te handelen

```javascript
function handleSubmission() {
  window.adobeDataLayer = window.adobeDataLayer || [];

  const selectedAssetClass = document.querySelector('input[name="assetclass"]:checked');
  const errorMessage = document.getElementById("error-message");
  const messageBox = document.getElementById("message");

  if (!selectedAssetClass) {
    errorMessage.textContent = "Please select a financial instrument.";
    messageBox.textContent = "";
    return;
  }

  errorMessage.textContent = "";

  const subscriptionEvent = {
    event: "assetClassSelection",
    xdm: {
      eventType: "assetClassSelection",
      eventID: "investment_preference_event",
      timestamp: new Date().toISOString(),
      FinancialInterest: {
        PreferredFinancialInstrument: selectedAssetClass.value
      }
    }
  };

  console.log("📩 Sending asset class data to AEP:", subscriptionEvent);
  window.adobeDataLayer.push(subscriptionEvent);

  // ✅ Show thank-you message
  messageBox.textContent = `Thank you for selecting "${selectedAssetClass.value}". We'll use this to personalize your experience.`;
}
```

[Het voorbeeld van het HTML-formulier is beschikbaar als onderdeel van deze zelfstudie](assets/webform.zip)
