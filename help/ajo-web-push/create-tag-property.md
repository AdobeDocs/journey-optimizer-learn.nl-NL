---
title: Tag maken, eigenschap
description: De eigenschap tag verzendt de gegevens van de browser naar de AEP via Web SDK.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-01-21T00:00:00Z
jira: KT-20879
source-git-commit: 3d342c5c4de4dda221ce4427b1e4aef7ef8c22cc
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# Tag maken, eigenschap

In het tweede deel van deze zelfstudie leert u hoe u pushmeldingen in real-time kunt activeren door handmatig een aangepaste price.drop-gebeurtenis te verzenden. Deze benadering gebruikt AEP Data Collection (Markeringen) om de gebeurtenis van de Web-pagina te vangen en het te verzenden naar Adobe Experience Platform. Zodra de gebeurtenis wordt opgenomen, leidt het een reis in Adobe Journey Optimizer, die u toestaat om pushberichten op bestelling te verzenden op gebruikersacties of bedrijfsgebeurtenissen wordt gebaseerd.

Deze eigenschap is geconfigureerd met de AEP Web SDK, die is verbonden met de `WebPushDataStream` die eerder in de zelfstudie is gemaakt. De markeringseigenschap luistert naar de `price.drop` -gebeurtenis op de Adobe Data Layer en wijst de relevante productdetails toe door het ProductListItems-gegevenselement bij te werken. Nadat de gegevens zijn voorbereid, wordt een regel in de eigenschap tag geactiveerd en wordt de gebeurtenis price.drop via het web SDK naar AEP verzonden. Deze gebeurtenis fungeert vervolgens als toegangspunt voor een reis in Adobe Journey Optimizer, waardoor pushberichten direct kunnen worden bezorgd op basis van de prijsdaling.

## Tagelementen

ProductListItems om productgegevens te bevatten

![&#x200B; markering-elementen &#x200B;](assets/product-list-items-element.png)

xdmvariable-toewijzing aan de `schemaForPushNotification`

![&#x200B; xdm-veranderlijk &#x200B;](assets/xdmvariable-data-element.png)

## Regel maken

De gebeurtenis price.drop beluisteren
![&#x200B; gegeven-duw-gebeurtenis &#x200B;](assets/tag-rule-event.png)

De productListItems bijwerken met de updatevariabele
![&#x200B; update-veranderlijk &#x200B;](assets/update-variable.png)
Verzend ten slotte de gebeurtenis price.drop naar AEP met de bijgewerkte xdmvariable
![&#x200B; send-event &#x200B;](assets/send-event.png)

De volgende javascript-code verzendt de gebeurtenis price.drop vanaf de webpagina naar AEP Tags

```javascript
 <script>
      window.adobeDataLayer.push({
        event: "price.drop",
        productListItems: productListItems
      });
  </script>
```



