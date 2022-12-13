---
title: Een bevestigingsbericht voor bestelling maken
description: Test uw kennis op hoe te om transactieverslagen tot stand te brengen en te personaliseren
kt: 7531
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: ec86e2ac-081d-47aa-a948-007107baa2b4
source-git-commit: cc9d123e4b8efd82eea348c31f5b993556438074
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 3%

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
1. Gebruik de gebeurtenis: [!DNL LumaOnlinePurchase] als trigger
1. Het opgeroepen bevestigingsbericht voor bestelling maken `Luma - Order Confirmation`:

* Transactie in categorie - zorg ervoor dat u het oppervlak voor transactie-e-mail selecteert
* De onderwerpregel moet zijn gepersonaliseerd met de voornaam van de ontvanger en de uitdrukking &quot;bedankt voor uw aankoop&quot; bevatten
* Gebruik de **Luma, overzicht van de volgorde** sjabloon en wijzigen:

De e-mail moet als volgt worden gestructureerd:
<table>
<tr>
<td>
  <div>
     <strong> Sectie Koptekst</strong>
      </div>
  </td>
  <td>
    <strong>Logo Luma</strong>
      <p>
     <li>luma_logo.png</li>
    <li>Grootte 35%, gecentreerde witte achtergrond </li>
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
    <strong>Image</strong><p>
    <li>luma-transactional-order-confirmation-2.jpg </li>
    <li>Marge: Boven, onder (10)<div>
    <p>
    <strong>Tekst</strong><p>
    <em>Hey {voornaam}</em><p>
    <li>Uitlijning: left  </li>
   <li>Tekstkleur: rgb(69, 97, 162) #4461a2; 
   <li>tekengrootte: 20 px</li>
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
      <p><li>Vervang het hard gecodeerde adres in het malplaatje met het adreslading van het profiel
      <li> De korting, Totaal, Ophalen verwijderen</p>
  </td>
  <td>
  <p> Verzenden naar:</p>
      <em>Achternaam voornaam<br>
      Straat<br>
      Plaats, Staat, Postcode</em></p>

    &lt;strong>Knop:&lt;/strong>&lt;/p>
<p><em>Bestelling weergeven</em></p>
      <li>Achtergrondkleur: rgb(25, 121, 195)</li>
      <li>Tekstkleur: Wit</li>
      <li>Geen rand</li>
      <li>Hoogte: 40</li>
      <li>Een koppeling toevoegen aan een door u gekozen website </li>
      <li>Links uitlijnen met de bovenstaande tekst (tip: de containermarge gebruiken)</li>
  </td>
 <tr>
<td>
  <div>
     <strong>Sectie Bestelgegevens</strong>
      </div>
       <p><li>Deze sectie toevoegen tussen de <b>Verzenden naar</b> en de <b>Volgorde weergeven</b> knop
      </p><br>
      <p><b>Tips:</b>
      <li>Dit is contextuele gebeurtenisinformatie.
      <li>Gebruik de functie [!UICONTROL helper]: [!UICONTROL each]
      <li>Schakel over naar de indeling van de code-editor om de contextuele gegevens toe te voegen.
      <li>Plaats de informatie in containers met DIV-tags.
  </td>
  <td>
    <strong>Koptekst</strong>
    <p>
    <em>Order {Purchase Order Number}</em>
    </p>
    <strong>Lijst met bestelde producten:
  </strong>
  <p>Elk van de items moet als volgt worden opgemaakt:
   <img alt="bestellen" src="./assets/c2-order.png"> 
</p>
<strong>Afbeelding van product:</strong>
<li>klasse: cart-item-stoel
<li>stijl: border-box: min-height:40 px</li>
<li>opvulling boven en onder:20 px</li>
<li>padding-left:80 px</li>
<li>border-radius:0 px</li>
<li>Als achtergrondafbeelding voor de container gebruiken</li>
<li>background-position: 0% 50%</li>
<li>background-size: 60 px</li>
<li>background-repeat: niet herhalen</li>
<p>
<strong>Prijs:</strong>
<li>Format = H5</li>
<li>style = box-sizing:border-box</li>
<li>margin-bottom:5 px</li>
<li>margin-top:0px;</li>
<p>
<strong>Naam en hoeveelheid:</strong>
<li>class=text-small</li>
<li>style=box-sizing: border-box</li>
<li>opvulling boven: 5 px</li>
<li>kleur: rgb(101, 106, 119)</li>
<li>font-size:14px</li>
<p>
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
   * Stel de profiel-id in op: Jenna_Palmer9530@emailsim.io
   * Type gebeurtenis: commerce.purchase
   * Naam: Sprite Yoga Companion Kit
   * Aantal: 1
   * Prijstotaal: 61
   * Volgnummer: 6253728
   * SKU: 24-WG080
   * productImageURL: <https://publish1034.adobedemo.com/content/dam/luma/en/products/gear/fitness-equipment/luma-yoga-kit-2.jpg>

U ontvangt het bevestigingsbericht voor een persoonlijke aankoop met het opgegeven product.

* De onderwerpregel moet beginnen met de voornaam van het testprofiel: Jenna
* De sectie met orderdetails moet worden gevuld met de orderdetails die u hebt ingevoerd tijdens het testen
* De gegevens van de klant moeten de plaats en de postcode van uw testprofiel hebben:

   43913 Thierer Terrace, Washington DC 2009



>[!TAB Uw werk controleren]

** Reis

![Reis](/help/challenges/assets/c2-journey.png)


** Email

**Onderwerpregel:**

{{ profile.person.name.firstName }}, dank u voor uw aankoop!


**Sectie met details van volgorde:**

![Sectie Bestelgegevens](/help/challenges/assets/c2-order-detail-section.png)

Zo ziet uw code eruit:

Koptekst:

```javascript
Order: {{context.journey.events.1627840522.commerce.order.purchaseOrderNumber}}
```

Lijst van producten:

Gebruik de hulpfunctie &quot;each&quot; om de lijst met producten te maken. Zo ziet uw code eruit:

```javascript
{{#each context.journey.events.1911672547.productListItems as|product|}}
<div class="cart-item-chair" style="box-sizing:border-box;min-height:40px;padding-top:20px;padding-bottom:20px;padding-left:80px;border-radius:0px;background-image:url({{product._wwfovlab065.productImageURL}});background-position:0% 50%;background-size:60px;background-repeat:no-repeat;">
<h5 style="box-sizing:border-box;margin-bottom:5px;font-size:16px;line-height:20px;margin-top:0px;">${{product.priceTotal}}.00</h5>
<div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">{{product.name}}</div><div class="text-small" style="box-sizing:border-box;padding-top:5px;color:rgb(101, 106, 119);font-size:14px;">Quantity: {{product.quantity}}</div></div><div class="divider-small" style="box-sizing:border-box;height:1px;margin-top:10px;margin-bottom:10px;background-color:rgb(209, 213, 223);"> </div>
{{/each}}

Total: ${{context.journey.events.1627840522.commerce.order.priceTotal}} 
```

**Sectie met klantgegevens**

![Adres van klant](assets/c2-customer-information.png)

De personalisatie moet er als volgt uitzien:

```javascript
{{profile.homeAddress.street1}}
{{profile.homeAddress.city}},{{profile.homeAddress.state}} {{profile.homeAddress.postalCode}}
```

>[!ENDTABS]