---
title: Een bevestigingsbericht voor een bestelling maken
description: Test uw kennis op hoe te om transactionele berichten tot stand te brengen en te personaliseren.
jira: KT-7531
feature: Journeys
role: User
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: 7861e0ca17a616273f5ea1b4d850310f1f4ec8b8
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 4%

---


# Een bevestigingsbericht voor een bestelling maken

| Uitdaging | Transactie-e-mail voor bevestiging van bestelling maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[E-mailcontent maken met de berichteneditor](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/create-content-with-the-email-designer.html?lang=nl-NL)</li> <li>[Contextuele gebeurtenisinformatie gebruiken voor personalisatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=nl-NL)</li><li>[Helpfuncties gebruiken voor personalisatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=nl-NL)</li></ul> |
| Te downloaden middelen | [Bevestigingsmiddelen bestellen](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

{style="table-layout:auto"}

## Het artikel

Luma lanceert hun online opslag en wil een goede klantenervaring verzekeren. Ze geven een bevestigingsbericht voor bestellingen wanneer een klant een bestelling heeft geplaatst.

## Uw uitdaging

Maak een reis die een bevestigingsbericht voor bestellingen verzendt wanneer een klant van een Luma een online bestelling voltooit.

>[!BEGINTABS]

>[!TAB Taak]

1. Een reis maken die `Luma - Order Confirmation`.

1. Gebruik de gebeurtenis: `LumaOnlinePurchase`.

1. Een **transactie**  email geroepen `Luma - Order Confirmation`.

   * De onderwerpregel &quot;Bedankt voor uw aankoop, `FirstName`&quot;

   * Gebruik de `Luma - Order summary` sjabloon en wijzigen:

      * Verwijder de `You may also like` secties

      * Voeg de koppeling voor afmelden onder aan de e-mail toe

De e-mail moet als volgt worden gestructureerd:

<table>
<tr>
<td>
  <div>
     <strong> Sectie Koptekst</strong>
      </div>
  </td>
  <td>
      <p>
     <li>luma_logo.png</li>
    <li>De link naar de luma-website: https://luma.enablementadobe.com/content/luma/us/en.html</li>
    <p>
    </td>
  </tr>
  <tr>
  <td>
  <div>
    <strong>Sectie voor bevestiging van bestelling
    </strong>
  </td>
  <td>
    <p>
    <strong>Tekst</strong><p>
    <em>Hé {firstName},</em><p>
   <div>
    <p>
     <em>Uw bestelling is geplaatst.
    <p>Zodra uw pakket is verzonden, sturen we u een e-mail met een trackingnummer, zodat u uw bestelling kunt volgen.</p></em>
    </strong>
    </tr>
  </td>
 <td>
  <div>
     <strong> Naar sectie</strong>
      </div>
      <p>
      <li>Voornaam en achternaam zijn afkomstig uit het profiel
      <li>Vervang het hard-gecodeerde adres in het malplaatje met <b>verzendadres</b>
      <li>De adresdetails zijn contextafhankelijke kenmerken van de gebeurtenis (straat 1, plaats, postcode, staat)
      <li> Verwijderen <i>Korting, totaal, aanschaffen</i></p>
  </td>
  <td>
  <p> Verzenden naar:</p>
      <em>{firstName} {lastName}<br>
     {Street 1}<br>
     {City}, {State} {postalCode}<br></em></p>
  </td>
 <tr>
<td>
  <div>
     <strong>Sectie Bestelgegevens</strong>
      </div>
       <p><li>Deze sectie toevoegen onder de sectie <b>Verzenden naar</b> sectie.
      </p><br>
      <p><b>Tips:</b>
      <li>De structuurcomponent gebruiken <b>1:2, kolom links</b> voor deze sectie
      <li>Dit is contextuele gebeurtenisinformatie.
      <li>Gebruik de hulpfunctie : [!UICONTROL each]
      <li>Schakel over naar de indeling van de code-editor om de contextuele gegevens toe te voegen.
  </td>
  <td>
    <strong>Koptekst</strong>
    <p>
  Volgorde: <em>{purchaseOrderNumber}</em>
    </p>
    <strong>Lijst met bestelde producten:
  </strong>
  <p>Geef elk product in de volgorde weer met een afbeelding, de prijs en de naam.
  <p>De lay-out van elk item moet er als volgt uitzien:
   <img alt="bestellen" src="./assets/c2-order.png"> 
<p><b>De koppeling naar het winkelwagentje toevoegen</b>
<p>Vervang de bestellings-id in de URL door het inkoopordernummer:
   <i>https://luma.enablementadobe.com/content/luma/us/en/user/account/order-history/order-details.html?orderId=90845952-c2ea-4872-8466-5289183e4607</i>
</td>
  </tr>
</table>

>[!TIP]
>
>Om u toe te staan om uw reizen problemen op te lossen, beste praktijken moeten een alternatieve weg aan alle berichtacties toevoegen als er een onderbreking of een fout is.

>[!TAB Succescriteria]

Trigger de Reis die u in testwijze creeerde en verzend e-mail naar me:

1. Voordat u overschakelt naar de testmodus, overschrijft u de parameters voor e-mail die u naar het teste-mailadres wilt verzenden.
   1. Open de weergave E-maildetails.
   1. Klik in het gedeelte E-mailparameters op het T-symbool (parameteroverschrijving inschakelen)
   1. Klik in het veld Adres
   1. Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: *&quot;yourname@yourdomain&quot;* in de uitdrukkingsredacteur en klik o.k.
1. Het traject in de testmodus zetten
1. De gebeurtenis activeren met de volgende parameters:
   * Stel de profiel-id in op: Identiteitswaarde:`a8f14eab3b483c2b96171b575ecd90b1`
   * Type gebeurtenis: commerce.purchase
   * `Quantity`: 1
   * `Price Total:` 69
   * `Purchase Order Number:` 90845952-c2ea-4872-8466-5289183e4607
   * `SKU:` LLMH09
   * `City:`San Jose
   * `Postal Code:` 95119
   * `State`: CA
   * `Street:` 245 Park Avenue

Je ontvangt het bevestigingsbericht voor een persoonlijke aankoop.

* De onderwerpregel moet de voornaam van het testprofiel hebben: Leora

* Zo ziet het e-mailadres eruit:

![E-mail](/help/challenges/assets/c2-email.png)

>[!TAB Uw werk controleren]

**Reis**

![Reis](/help/challenges/assets/c2-journey.png)


**E-mail**

**Onderwerpregel:**

Bedankt voor uw aankoop, `{{ profile.person.name.firstName }}`!

**Naar sectie verzenden:**

Zo ziet uw code eruit:

```javascript
{{ profile.person.name.firstName }} {{ profile.person.name.lastName }}
{{context.journey.events.454181416.commerce.shipping.address.street1}}
{{context.journey.events.454181416.commerce.shipping.address.city}}, {{context.journey.events.454181416.commerce.shipping.address.state}} {{context.journey.events.454181416.commerce.shipping.address.postalCode}}
```

*event.45481416* Dit is een ander nummer voor jou.

TIP: elke regel afzonderlijk aanpassen

**Sectie met orderdetails:**

Zo ziet uw code eruit:

Koptekst:

```javascript
Order #: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

**Lijst van producten:**

Gebruik de hulpfunctie &quot;each&quot; om de lijst met producten te maken. Geef deze weer in een tabel. Zo moet uw code eruit zien (met specifieke variabelen zoals uw gebeurtenis-id) in plaats van `454181416` en uw organisatie I in plaats van `techmarketingdemos` ):

```javascript
{{#each context.journey.events.454181416.productListItems as |product|}}<tr> <th class="colspan33"><div class="acr-fragment acr-component image-container" data-component-id="image" style="width:100%;text-align:center;" contenteditable="false"><!--[if mso]><table cellpadding="0" cellspacing="0" border="0" width="100%"><tr><td style="text-align: center;" ><![endif]--><img src="{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.imageUrl}}" style="height:auto;width:100%;" height="233" width="233"><!--[if mso]></td></tr></table><![endif]--></div></th> <th class="colspan66"><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p><span style="font-weight:700;">{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.name}}</span></p></div></div><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p>${{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.price}}.00</p></div></div></th></tr> {{/each}}
```

**Knop voor weergavevolgorde:**

`https://luma.enablementadobe.com/content/luma/us/en/user/account/order-history/order-details.html?orderId={{context.journey.events.454181416.commerce.order.purchaseOrderNumber}}`

**Totaalprijs:**

Totaal:`${{context.journey.events.1627840522.commerce.order.priceTotal}}.00`


>[!ENDTABS]