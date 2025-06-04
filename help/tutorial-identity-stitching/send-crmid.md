---
title: Bouw de steekproeftoepassing om login activiteit na te bootsen
description: Bouw een steekproefNode.js toepassing om een login stroom te simuleren
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: e080149c-0ac0-4559-b99d-ebad9f03b98b
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Bouw de steekproeftoepassing om login activiteit na te bootsen

Deze voorbeeldtoepassing, die op een server Node.js wordt gebouwd en opgesteld, toont aan hoe te om een identiteitskaart van CRM naar Adobe Experience Platform (AEP) te verzenden wanneer een gebruiker login. De toepassing simuleert een aanmeldstroom waarbij gebruikersgegevens op de server worden gevalideerd. Na een geslaagde aanmelding wordt de CRM-id van de gebruiker opgehaald en naar de adobeDataLayer geduwd, waardoor een corresponderende regel wordt geactiveerd in Adobe Experience Platform-tags (voorheen Adobe Launch).

De attachLoginHandler-functie koppelt een verzendgebeurtenislistener aan een aanmeldingsformulier. Bij het verzenden van formulieren voorkomt dit de standaardhandeling, valideert het de referenties tegen het object van een vooraf gedefinieerde gebruiker en haalt het CRM-id op als dit geldig is. De functie duwt een gebruikersloged in gebeurtenis met identiteitskaart van CRM en authentificatiestatus aan adobeDataLayer, en de Markeringen van Adobe Experience Platform halen het op om de gegevens naar Adobe Experience Platform (AEP) te verzenden.


```javascript
function attachLoginHandler() {
    const form = document.getElementById("loginForm");
    if (!form) return;

    form.addEventListener("submit", function(e) {
        e.preventDefault();
        const username = document.getElementById("username").value;
        const password = document.getElementById("password").value;

        if (users[username] && users[username].password === password) {
            const crmid = users[username].crmid;
            window.adobeDataLayer = window.adobeDataLayer || [];
            debugger;
            window.adobeDataLayer.push({
                event: "userloggedin",
                user: {
                    crmid: crmid,
                    authenticatedState: "authenticated"
                }
            });
        }
    });
}
```

Het Adobe Experience Platform-tagscript wordt meestal als volgt opgenomen in de sectie `<head>` van de HTML-pagina met een `<script>` -tag:

`<script src="https://assets.adobedtm.com/b5eu4857867/4e4d84957/launch-b69e276bb9b5-development.min.js" async crossorigin="anonymous"></script>`

Het AEP-script voor tags is verkregen door een Web SDK-eigenschap te publiceren die in de eerdere stap is gemaakt en de insluitcode te kopiëren vanaf het tabblad Environment.
