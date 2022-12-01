---
title: Uitdaging voor productvervanging
description: Pas toe wat u hebt geleerd over het maken van segmenten en test uw vaardigheden.
kt: 8417
feature: Segments
role: User
level: Beginner
hide: true
exl-id: 305aaf4c-7f5d-4f6f-abeb-466208f1fe48
source-git-commit: 0e83d8fbad6bd87ed25980251970898cb5b94bc0
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 1%

---

# Uitdaging voor productvervanging

| Uitdaging | Productvervanging |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[Segmenten maken](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-segments.html?lang=en)</li><li> [HTML-e-mailcontent importeren en opstellen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/import-and-author-html-email-content.html?lang=en)</li><li>[Gebruiksscenario - Leessegment](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| Te downloaden middelen | [E-mailbestanden voor seizoensgebonden verzameling](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## Het artikel

Wanneer klanten op de Luma-website bladeren, kunnen ze producten toevoegen die ze graag willen zien. Dit staat Luma toe om de klanten gerichte marketing berichten en informatie over de producten te verzenden.

## Uw uitdaging

Luma vraagt u om een reis in Journey Optimizer uit te voeren die klanten op de hoogte brengt, die een punt op hun verlanglijst hebben dat eerder verouderd was, wanneer dit punt weer in voorraad is.

## Definieer het segment - items in de Wishlist-lijst buiten de voorraad

Om potentiële geïnteresseerde klanten te richten wanneer de producten worden herbevolkt, creeer een segment dat uit klanten bestaat

* Wie ten minste één item aan hun verlanglijst heeft toegevoegd (gebeurtenistype gebruiken: [!UICONTROL Opslaan voor later])
* Welke **uit voorraad** in de laatste drie maanden (gebruik voorraad = 0)
* En heb het object sindsdien niet gekocht.

Geef dit segment een naam: *uw naam - Verouderd*

+++**UW WERK CONTROLEREN**

Zo ziet uw segment eruit:

![Segment - Afzonderlijke items op de Wishlist](/help/challenges/assets/C1-S2.png)

Klanten die een item aan hun verlanglijst hebben toegevoegd dat de afgelopen drie maanden uit voorraad was:

* Gebeurtenis: Opslaan voor later
   * Inclusief minimaal 1
   * Wanneer de voorraadhoeveelheid gelijk is aan 0

en het object sindsdien niet hebben gekocht:

* Sluit alle de gebeurtenistypen van Aankopen uit waar SKU SKU van SKU van **De gebeurtenis Opslaan voor later**.

>[!TIP]
> * Selecteer de SKU onder Opslaan voor later in het dialoogvenster *Door variabelen bladeren* sectie
> * Gebruik de vergelijkingsoptie wanneer u de SKU onder Opslaan voor later in het gebeurtenisveld plaatst


Controleer de code in de rechterbenedenhoek van het scherm Segment bewerken onder Gebeurtenissen. De code moet er als volgt uitzien:

Code:
```(Include have at least 1 Save For Laters event where ((Stock Quantity equals 0)) THENExclude all  Purchases events where ((SKU equals Save For Laters1 SKU)) ) and occurs in last 3 month(s)```

+++

### E-mail maken - Luminantiefunctie voor productvervanging

Klanten op de hoogte stellen die een product uit de voorraad hebben toegevoegd met een oproep om te gaan winkelen, nu het product weer in voorraad is.

### Maak een reis - kennisgeving van de productvoorraad

Wanneer een eerder out-of-stock item weer in voorraad is, geeft u klanten die een out-of-stock item hadden toegevoegd een oproep om te gaan winkelen, nu het item weer in voorraad is.

1. Een reis maken met de naam &quot;uw naam_Luma - Productherstart
1. De reis moet worden gestart wanneer een product weer in voorraad is
1. Verzend de *Luminageproduct vervangen* e-mailen naar
1. Gebruikers die dit item aan hun verlanglijst hadden toegevoegd terwijl het uit voorraad was

>[!TIP]
>
> Gebruik de bestaande bedrijfsgebeurtenis. U moet een voorwaarde toevoegen die controleert dat restock SKU inbegrepen in (om het even welk) gebeurtenistype sparen voor Lagen is.

+++**SUCCESCRITERIA**

Test uw reis:

1. Zorg ervoor dat de segmentkwalificatiegebeurtenis Namespace = Email heeft
1. Hef de standaard e-mailparameters op en stel deze in op uw eigen e-mailadres (zie e-mail nr. 1 voor instructies).
1. De overgang naar de testmodus instellen
1. Trigger een gebeurtenis - ga de volgende gegevens in:

   * Omschrijving: Vergeet de mooie machines en dure lidmaatschappen - de Harmony Lumaflex Sterkte Band Kit is alles wat u nodig hebt voor een geweldige werkout. De kit bevat alles wat u nodig hebt voor een reeks oefeningen voor versterking en kleurtonen.
   * Naam: Harmony Lumaflex Strength Band Kit
   * Prijs: 22
   * Product-id: 24-UG03
   * URL afbeelding product: https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/ug03-bk-0.jpSKU: 24-UG03
   * Type voorraadgebeurtenis: herbevoorraden
   * Profiel-id: Jenna_Palmer9530@emailsim.io

U ontvangt de e-mail &quot;Luma Email Product Replenging&quot; met de productgegevens en de personalisatie voor Wenen.

+++

+++**UW WERK CONTROLEREN**

Zo ziet uw reis eruit:

![Reis voor productaanvulling](/help/challenges/assets/c3-j3-journey.png)

Voorwaarde: In verlanglijst

![Voorwaarde - in wenslijst](/help/challenges/assets/c3-j3-condition.png)

Voorwaardencode:

```in(@{LumaProductRestock._wwfovlab065.sku},#{ExperiencePlatform.ExperienceEvents.experienceevent.all(currentDataPackField.eventType=="commerce.saveForLaters").productListItems.all().SKU})```

+++
