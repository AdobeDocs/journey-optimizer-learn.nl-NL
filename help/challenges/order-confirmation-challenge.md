---
title: Een bevestigingsbericht voor bestelling maken
description: Test uw kennis op hoe te om transactieverslagen tot stand te brengen en te personaliseren
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: 70815c3cd30de22aad7ec667b8baf9b4c8642491
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 4%

---


# Een bevestigingsbericht voor bestelling maken

![Bevestiging van bestelling](/help/challenges/assets/email-assets/luma-transactional-order-confirmation.png)

| Uitdaging | Transactie-e-mail voor bevestiging van bestelling maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[E-mailcontent maken met de berichteneditor](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[Contextuele gebeurtenisinformatie gebruiken voor personalisatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[Helpfuncties gebruiken voor personalisatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| Te downloaden middelen | [Bevestigingsmiddelen bestellen](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## Het artikel

Luma, start hun online winkel en wil een goede klantenervaring verzekeren door een bevestigingsbericht van de orde te verstrekken zodra een klant een orde heeft geplaatst.



## Uw uitdaging

Maak een reis die een bevestigingsbericht voor bestellingen verzendt wanneer een klant van een Luma een online bestelling voltooit.

>[!BEGINTABS]

>[!TAB Taak]

1. Een reis maken met de naam `Luma - Order Confirmation`
2. Gebruik de gebeurtenis: `LumaOnlinePurchase`
3. Het opgeroepen bevestigingsbericht voor bestelling maken `Luma - Order Confirmation`:

* Transactie in categorie - zorg ervoor dat u het oppervlak voor transactie-e-mail selecteert
* De onderwerpregel moet zijn gepersonaliseerd met de voornaam van de ontvanger en de uitdrukking &quot;bedankt voor uw aankoop&quot; bevatten
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
    <li>De website moet een link hebben naar de lumawebsite: https://publish1034.adobedemo.com/content/luma/us/en.html</li>
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
    <em>Hey {firstName}</em><p>
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
      <li>Vervang het hard gecodeerde adres in het malplaatje met <b>verzendadres</b>
      <li>De adresdetails zijn contextafhankelijke kenmerken van de gebeurtenis (straat 1, plaats, postcode, staat)
      <li> De korting, Totaal, Ophalen verwijderen</p>
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
      <li>Gebruik de structuurcomponent "1:2 column left" voor deze sectie
      <li>Dit is contextuele gebeurtenisinformatie.
      <li>Gebruik de functie [!UICONTROL helper]: [!UICONTROL each]
      <li>Schakel over naar de indeling van de code-editor om de contextuele gegevens toe te voegen.
  </td>
  <td>
    <strong>Koptekst</strong>
    <p>
    <em>Volgorde: ` purchaseOrderNumber`</em>
    </p>
    <strong>Lijst met bestelde producten:
  </strong>
  <p>Elk van de items moet als volgt worden opgemaakt:
   <img alt="bestellen" src="./assets/c2-order.png"> 
</p>
</td>
  </tr>
</table>


>[!TIP]
>
>Om u toe te staan om uw reizen problemen op te lossen, beste praktijken moeten een alternatief weg aan alle berichtacties in het geval van onderbreking of fout toevoegen.

>[!TAB Succescriteria]

Trigger de Reis u op testwijze creeerde en verzend e-mail naar me:

1. Verborgen waarden weergeven door op het oogsymbool te klikken:
   1. Klik in de e-mailparameters op het T-symbool (schakel parameteroverschrijving in)
      ![E-mailparameters overschrijven](/help/challenges/assets/c3-override-email-paramters.jpg)
   2. Klik in het veld Adres
   3. Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: *yourname@yourdomain* in de uitdrukkingsredacteur en klik o.k.
2. Het traject in testmodus zetten
3. De gebeurtenis activeren met de volgende parameters:
   * Stel de profiel-id in op: Identiteitswaarde:`a8f14eab3b483c2b96171b575ecd90b1`
   * Type gebeurtenis: commerce.purchase
   * `Quantity`: 1
   * `Price Total:` 69
   * `Purchase Order Number:` 6253728
   * `SKU:` LLMH09
   * `City:` Washington
   * `Postal Code:` 20099
   * `State`: DC
   * `Street:` Thierer Terrace

U ontvangt het bevestigingsbericht voor een persoonlijke aankoop met het opgegeven product.

* De onderwerpregel moet de voornaam van het testprofiel hebben: Leora
* De sectie met orderdetails moet worden gevuld met de orderdetails die u hebt ingevoerd tijdens het testen

>[!TAB Uw werk controleren]

**Reis**

![Reis](/help/challenges/assets/c2-journey.png)


**E-mail**

**Onderwerpregel:**

Bedankt voor uw aankoop, {{ profile.person.name.firstName }}!

Zo ziet het e-mailadres eruit:

![E-mail](//help/challenges/assets/c2-email.png)

**Naar sectie verzenden:**

Zo ziet uw code eruit:

```javascript
{{ profile.person.name.firstName }} {{ profile.person.name.lastName }}
{{context.journey.events.454181416.commerce.shipping.address.street1}}
{{context.journey.events.454181416.commerce.shipping.address.city}}, {{context.journey.events.454181416.commerce.shipping.address.state}} {{context.journey.events.454181416.commerce.shipping.address.postalCode}}
```

*event.45481416* wordt een ander nummer voor u.

TIP: Elke regel afzonderlijk aanpassen

**Sectie met details van volgorde:**

Zo ziet uw code eruit:

Koptekst:

```javascript
Order #: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

**Lijst van producten:**

Gebruik de hulpfunctie &quot;each&quot; om de lijst met producten te maken. Geef deze weer in een tabel. Zo moet uw code eruit zien (met specifieke variabelen zoals uw gebeurtenis-id) in plaats van `454181416` en uw organisatie I in plaats van `techmarketingdemos` ):

```javascript
{{#each context.journey.events.454181416.productListItems as |product|}}<tr> <th class="colspan33"><div class="acr-fragment acr-component image-container" data-component-id="image" style="width:100%;text-align:center;" contenteditable="false"><!--[if mso]><table cellpadding="0" cellspacing="0" border="0" width="100%"><tr><td style="text-align: center;" ><![endif]--><img src="{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.imageUrl}}" style="height:auto;width:100%;" height="233" width="233"><!--[if mso]></td></tr></table><![endif]--></div></th> <th class="colspan66"><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p><span style="font-weight:700;">{{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.name}}</span></p></div></div><div class="acr-fragment acr-component" data-component-id="text" contenteditable="false"><div class="text-container" contenteditable="true"><p>${{context.journey.events.454181416.productListItems.VYG__902489191a0a40e67f51f17f3ea9e2dfaf2dea3bd0bebe8b._techmarketingdemos.product.price}}.00</p><p>Quantity: {{context.journey.events.454181416.productListItems.quantity}}</p></div></div></th></tr> {{/each}}
```

**Totaalprijs:**

Totaal:`${{context.journey.events.1627840522.commerce.order.priceTotal}}.00`


>[!ENDTABS]