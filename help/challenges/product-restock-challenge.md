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
source-git-commit: 5c763ec877c75c07132f4cc714d63695e12638dc
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 2%

---

# Uitdaging voor productvervanging

| Uitdaging | Productvervanging |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[Segmenten maken](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=nl-NL)</li><li> [HTML-e-mailcontent importeren en opstellen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html?lang=nl-NL)</li><li>[Gebruiksscenario - Leessegment](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=nl-NL)</li> |
| Te downloaden middelen | [E-mailbestand voor productvoorraad](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip) |

## Het artikel

Wanneer klanten op de Luma-website bladeren, kunnen ze producten toevoegen die ze graag willen zien, zodat Luma de klanten gerichte marketingberichten en informatie over de producten kan sturen.

## Uw uitdaging

Luma vraagt u om een reis in Journey Optimizer uit te voeren die klanten op de hoogte brengt, die een punt op hun verlanglijst hebben dat eerder verouderd was, wanneer dit punt weer in voorraad is. Het creatieve team biedt u de [E-mailbestand voor productvoorraad](/help/challenges/assets/email-assets/ProductRestockEmail.html.zip).

>[!BEGINTABS]

>[!TAB Taak]

## 1. Definieer het segment - Afzonderlijke items op de weergavelijst

Om potentiële geïnteresseerde klanten te richten wanneer de producten worden herbevolkt, creeer een publiek dat uit klanten bestaat:

* Wie ten minste één item aan hun verlanglijst heeft toegevoegd (gebruik het gebeurtenistype: [!UICONTROL Opslaan voor later])
* die in de laatste drie maanden niet meer in voorraad was (voorraadhoeveelheid = 0)
* En heb het object sindsdien niet gekocht.

>[!TIP]
>Sluit alle de gebeurtenistypen van Aankopen uit waar SKU SKU van SKU van *De gebeurtenis Opslaan voor later*. U kunt het veld vinden in het dialoogvenster *Door variabelen bladeren* sectie.

Geef dit segment een naam: `Out-of-stock-Wishlist`


### 2. Maak een reis - kennisgeving van de productvoorraad

Wanneer een eerder out-of-stock item weer in voorraad is, geeft u klanten die een out-of-stock item hadden toegevoegd een oproep om te gaan winkelen, nu het item weer in voorraad is.

1. Bel de reis: `Product Restock`
2. De reis moet worden gestart wanneer een product weer in voorraad is
3. Verzend de *E-mailadres voor productvoorraad* tot
4. Gebruikers die dit item aan hun verlanglijst hadden toegevoegd terwijl het uit voorraad was

>[!TAB Succescriteria]

Test uw reis:

1. Zorg ervoor dat de gebeurtenis van het gelezen segment de Namespace = heeft `Luma CRM ID`
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

>[!TAB Uw werk controleren]

Zo ziet uw segment eruit:

![Segment - Afzonderlijke items op de Wishlist](/help/challenges/assets/C1-S2.png)


Zo ziet uw reis eruit:

![Reis voor productaanvulling](/help/challenges/assets/c3-j3-journey.png)

Voorwaarde: in verlanglijst

![Voorwaarde - in wenslijst](/help/challenges/assets/c3-j3-condition.png)

Voorwaardencode:

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```


>[!TIP]
> * Selecteer de SKU onder Opslaan voor later in het dialoogvenster *Door variabelen bladeren* sectie
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




