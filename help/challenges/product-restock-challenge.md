---
title: Uitdaging voor productvervanging
description: Pas toe wat u hebt geleerd over het maken van segmenten en test uw vaardigheden.
jira: KT-8417
feature: Segments
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 201470e35095b38617d1a1bb5d7b16c1e60f431e
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Uitdaging voor productvervanging

| Uitdaging | Productvervanging |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[&#x200B; creeer segmenten &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=nl-NL)</li><li> [&#x200B; de Invoer en auteurHTML e-mailinhoud &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=nl-NL)</li><li>[&#x200B; Geval van het Gebruik - Gelezen segment &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journeys/use-case-read-segment.html?lang=nl-NL)</li> |
| Assets downloaden | [&#x200B; de restock e-maildossier van het Product &#x200B;](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip) |

## Het artikel

Wanneer klanten op de Luma-website bladeren, kunnen ze producten toevoegen die ze graag willen zien, zodat Luma de klanten gerichte marketingberichten en informatie over de producten kan sturen.

## Uw uitdaging

Luma vraagt u om een reis in Journey Optimizer uit te voeren die klanten op de hoogte brengt, die een punt op hun verlanglijst hebben dat eerder verouderd was, wanneer dit punt weer in voorraad is. Het creatieve team voorziet u van het [&#x200B; dossier van het Product restock e-mail &#x200B;](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip).

>[!BEGINTABS]

>[!TAB Taak]

## &#x200B;1. Definieer het segment - Afzonderlijke items op de weergavelijst

Om potentiële geïnteresseerde klanten te richten wanneer de producten worden herbevolkt, creeer een publiek dat uit klanten bestaat:

* Die minstens één punt aan hun verlanglijst (gebruik het gebeurtenistype: [!UICONTROL &#x200B; Commerce sparen voor Lagen &#x200B;]) hebben toegevoegd
* die in de laatste drie maanden niet meer in voorraad was (voorraadhoeveelheid = 0)
* En heb het object sindsdien niet gekocht.

>[!TIP]
>Sluit alle de gebeurtenistypen van Aankopen uit waar SKU SKU SKU van *sparen voor recentere gebeurtenis* aanpast. U kunt het gebied in *vinden doorbladert Variabelen* sectie.

Geef dit segment een naam: `Out-of-stock-Wishlist`


### &#x200B;2. Maak een reis - kennisgeving van de productvoorraad

Wanneer een eerder out-of-stock item weer in voorraad is, geeft u klanten die een out-of-stock item hadden toegevoegd een oproep om te gaan winkelen, nu het item weer in voorraad is.

1. Roep de reis aan: `Product Restock`
2. De reis moet worden gestart wanneer een product weer in voorraad is
3. Verzend het *e-mail van de Restock van het Product* aan
4. Gebruikers die dit item aan hun verlanglijst hadden toegevoegd terwijl het uit voorraad was

>[!TAB  criteria van het Succes ]

Test uw reis:

1. Zorg ervoor dat de gebeurtenis van het gelezen segment de Namespace = `Luma CRM ID` heeft
1. Hef de standaard e-mailparameters op en stel deze in op uw eigen e-mailadres (zie e-mail nr. 1 voor instructies).
1. De overgang naar de testmodus instellen
1. Trigger een gebeurtenis - ga de volgende gegevens in:

   * Beschrijving: Vergeet favoriete machines en dure lidmaatschappen - de Harmony Lumaflex Sterke Band Kit is alles wat u nodig hebt voor een geweldige werkout. De kit bevat alles wat u nodig hebt voor een reeks oefeningen voor versterking en kleurtonen.
   * Naam: Harmony Lumaflex Strength Band Kit
   * Prijs: 22
   * Product-ID: 24-UG03
   * URL van productafbeelding: https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/ug03-bk-0.jpSKU: 24-UG03
   * Type aandelengebeurtenis: voorraad
   * Profiel-id: Jenna_Palmer9530@emailsim.io

U ontvangt de e-mail &quot;Luma Email Product Replenging&quot; met de productgegevens en de personalisatie voor Wenen.

>[!TAB  Controle uw werk ]

Zo ziet uw segment eruit:

![&#x200B; Segment - uit-van-voorraad de Punten van Wishlist &#x200B;](/help/challenges/assets/C1-S2.png)


Zo ziet uw reis eruit:

![&#x200B; reis van de aanvulling van het Product &#x200B;](/help/challenges/assets/c3-j3-journey.png)

Voorwaarde: in verlanglijst

![&#x200B; Voorwaarde - in wenslijst &#x200B;](/help/challenges/assets/c3-j3-condition.png)

Voorwaardencode:

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```


>[!TIP]
> * Selecteer SKU onder Save for Laters in *doorbladert Variabelen* sectie
> * Gebruik de vergelijkingsoptie wanneer u de SKU onder Opslaan voor later in het gebeurtenisveld plaatst

Controleer de code in de rechterbenedenhoek van het scherm Segment bewerken onder Gebeurtenissen. De code moet er als volgt uitzien:

Code:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

>[!ENDTABS]

### E-mail maken - Luminantiedetail

Klanten op de hoogte stellen die een product uit de voorraad hebben toegevoegd met een oproep om te gaan winkelen, nu het product weer in voorraad is.



>[!TIP]
>
> Gebruik de bestaande bedrijfsgebeurtenis. Voeg een voorwaarde toe die controleert dat restock SKU in (om het even welk) gebeurtenistype sparen voor laters inbegrepen is.
>




