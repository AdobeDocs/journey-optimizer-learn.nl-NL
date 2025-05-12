---
title: Creeer een Web-pagina om de Oplossing te testen
description: Web-pagina om de gepersonaliseerde aanbiedingen te testen die gebruikend besluit worden geleverd.
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-05T00:00:00Z
jira: KT-17728
exl-id: 72a67137-303d-4dfe-9b70-322c81e5fb27
source-git-commit: 9a35160921988103182815efd3551151c09b9bb4
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Een webpagina maken om de oplossing te testen

Deze webpagina is gemaakt om gepersonaliseerde aanbiedingen te testen die via Adobe Journey Optimizer Decisioning worden aangeboden. Het verstrekt een gecontroleerd milieu waar de sendEvent vraag kan worden teweeggebracht en de teruggekeerde aanbiedingsinhoud teruggegeven, die de opstelling van de verpersoonlijking van begin tot eind helpen bevestigen en ervoor zorgen dat de beslissing zoals verwacht werkt.

Het volgende script is verantwoordelijk voor het ophalen en weergeven van een gepersonaliseerde aanbieding op een webpagina met Adobe Journey Optimizer.

1. HTML-entiteiten decoderen:

   Er is een hulpfunctie die speciale karakters in de aanbiedingsinhoud veilig omzet in leesbare HTML.

1. Personalisatie uitvoeren:

   Wanneer het geroepen, verzendt het een verzoek (`sendEvent`) naar het Web SDK van Adobe om gepersonaliseerde inhoud voor een specifiek gebied op de pagina (het `#ajo-offer` element) te krijgen.

   Als een aanbieding wordt geretourneerd, wordt de HTML gedecodeerd en op de pagina ingevoegd.

   Als niets is teruggekeerd, registreert het een waarschuwing.

1. Wacht op de SDK:

   Aangezien Adobe SDK (legering) asynchroon laadt, wacht het manuscript tot het volledig geladen alvorens het verzoek te doen.

   Het controleert om de 200 milliseconden, tot 20 keer, legering om fouten te vermijden.

1. Bij laden van pagina:

   Wanneer de pagina klaar is met laden, start het script het proces door `waitForAlloy()` aan te roepen.



```javascript
< script >
    function decodeHtmlEntities(html) {
        const txt = document.createElement("textarea");
        txt.innerHTML = html;
        return txt.value;
    }


function runPersonalization() {
    console.log("🚀 Sending personalization request to AJO...");
    alloy("sendEvent", {
        renderDecisions: true,
        personalization: {
            surfaces: ["#ajo-offer"]
        }
    }).then(result => {
        console.log("🔍 Web SDK decision response:", result);

        const decision = result.propositions?.[0];
        const html = decision?.items?.[0]?.data?.content;

        const container = document.getElementById("ajo-offer");
        if (html && container) {
            const decodedHtml = decodeHtmlEntities(html);
            console.log("✅ Offer HTML content (decoded):", decodedHtml);
            container.innerHTML = decodedHtml;
        } else {
            console.warn("⚠️ No personalized offer returned.");
        }


    }).catch(error => {
        console.error("❌ sendEvent failed:", error);
    });
}

function waitForAlloy(callback, retries = 20) {
    if (typeof alloy === "function") {
        callback();
    } else if (retries > 0) {
        console.log("⌛ Waiting for Alloy...");
        setTimeout(() => waitForAlloy(callback, retries - 1), 200);
    } else {
        console.error("❌ alloy is not loaded after waiting.");
    }
}

// Trigger initial personalization on page load
document.addEventListener("DOMContentLoaded", function() {
    waitForAlloy(() => runPersonalization());
}); <
/script>
```

[De voorbeeld-HTML-pagina en verwante middelen kunnen hier worden gedownload](assets/web-page-assets.zip)
