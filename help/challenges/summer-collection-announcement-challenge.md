---
title: Een mededeling over een zomerverzameling maken - Uitdaging
description: Verzend een mededeling van de zomerinzameling aan een segment van bestaande klanten' om de nieuwe inzameling van de zomer van de Luma te bevorderen.
kt: 8109
role: User
level: Beginner
last-substantial-update: 2022-11-16T00:00:00Z
hide: true
exl-id: ae457be7-2c67-4950-a072-1d7030b0e17b
source-git-commit: 8e79a4e474e3b6fc7692578fb2d5920e0772d9b0
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 1%

---

# Een mededeling over een zomerverzameling maken - Uitdaging

![Aankondigingsbanner voor AJO Summer Collection](/help/challenges/assets/email-assets/luma-transactional-onboarding-3.png)

| Uitdaging | Aankondiging zomerverzameling maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[Segmenten maken](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=en)</li><li> [HTML-e-mailcontent importeren en opstellen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=en)</li><li>[Gebruiksscenario - Leessegment](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| Te downloaden middelen | [E-mailbestanden voor seizoensgebonden verzameling](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

## Het artikel

Luma, een fictioneel atletisch kledingbedrijf, wil zijn nieuwste kleding- en tandwielcollectie promoten en de verkoop voor bestaande klanten stimuleren. Luma lanceert de nieuwe zomerinzameling en zou verschillende klantensegmenten specifiek willen richten.

## Uw uitdaging

Het marketingteam van Luma vraagt u om een marketingcampagne voor de zomerverzameling in Journey Optimizer uit te voeren. Uw uitdaging is:

* Maak een segment waarin wordt gedefinieerd welke profielen in aanmerking komen om de speciale actie te ontvangen.
* De reis maken

### Stap 1: Het segment definiëren - actieve klanten

>[!BEGINTABS]

>[!TAB Taak]

#### Een segment maken in Journey Optimizer

* Een segment maken met de naam Journey Optimizer `Active Customers`.
* Het segment moet alleen actieve Luma-klanten bevatten.
* Actieve klanten worden gedefinieerd als klanten met een laag in het loyaliteitsprogramma van Luma (zilver, goud, platina of diamant).


>[!TAB Succescriteria]

In de segmentbouwer, kunt u het geschatte aantal gekwalificeerde profielen zien. Als u met de gegevens van de trainingssandbox werkt, hebt u ongeveer 753 gekwalificeerde profielen van 1,29 kB.

>[!NOTE]
>Het kan tot 24 uren duren voor het segmentlidmaatschap voor bestaande profielen verschijnt, aangezien de bestaande profielen moeten worden teruggevuld.

**Er is een in aanmerking komend profiel toegevoegd aan het segment:**

U kunt controleren de profielen die aan het segment zijn toegevoegd kwalificeren door aan één van in de profielen te navigeren die op de mening van het Detail van uw Segment worden vermeld.

Controleer op de profielpagina de [!UICONTROL Attributen] om te bevestigen dat zij in aanmerking komen: De laag moet zilver, goud, platina of diamant zijn.

![Profielkenmerken](assets/C1-S1-profile-attributes.png)

U kunt ook de [!UICONTROL Segmentlidmaatschap] tab: Uw segment moet worden vermeld.

![Segmentlidmaatschap](assets/C1-S1-profile-segment-membership.png)

>[!TAB Uw werk controleren]

Segmentvelden: [!UICONTROL Attributen] > [!UICONTROL Afzonderlijk XDM-profiel] > [!UICONTROL Loyalty] > [!UICONTROL Tier]

Zo ziet uw segment eruit:

![Segment - Actieve klanten](/help/challenges/assets/C1-S1.png)

De code moet er als volgt uitzien:

```javascript
stringCompare("equals", loyalty.tier, ["diamond", "gold", "platinum", "silver"], false)
```

>[!ENDTABS]


### Stap 2: Aankondiging van de verzameling Journey - Summer

>[!BEGINTABS]

>[!TAB Taak]

#### Verstuur een aankondiging van de zomerinzameling

Een bureau heeft u vier HTML-bestanden geleverd met het ontwerp voor de e-mails:

* SeasonalCollectionEmail.html
* E-mail verzameling Luma Men&#39;s
* E-mail over verzameling van vrouwen in de luminantie
* Luminantie - 20 % korting op e-mail verzameling

1. [De e-mailbestanden voor seizoensverzamelingen downloaden](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip).

2. Een reis maken met de naam `Luma - Summer collection announcement` op basis van de volgende richtsnoeren :

   1. Verzenden *Luma - Nieuwe mededeling over de zomerverzameling* e-mailen naar *Actieve klanten* segment, dat 10% van het publiek als controlegroep uithoudt
      * Berichttitel `Luma - Summer Collection Announcement`.
      * Onderwerpregel `(recipient's first name), the new Luma summer collection is here!`.
      * Het opgegeven HTML-bestand gebruiken *SeasonalCollectionEmail.html* voor de e-mailhoofdtekst.
   2. Wacht twee dagen en verzend een vervolgbericht met meer gerichte inhoud:
      * Mannelijke klanten moeten de **Luma Men&#39;s Collection** e-mail.
         * Berichttitel: `Luma Men's Collection`
         * Onderwerpregel: `(recipient's first name), explore Men's New athletic gear!`
         * Hoofdtekst van e-mail: *MensCollectionEmail.html* voor de e-mailhoofdtekst.
      * Vrouwelijke klanten moeten de **Luma Women&#39;s Collection** e-mail.
         * Berichttitel: `Luma Women's Collection`
         * Onderwerpregel: `(recipient's first name), explore Luma's Women Collection!`
         * Hoofdtekst van e-mail: *WomensCollectionEmail.html*
      * Andere klanten moeten de **Luma - 20 % korting op collectie** e-mail.
         * Berichttitel: `Luma - 20 % off Collection`
         * Onderwerpregel: `(recipient's first name), enjoy 20% off sales!`
         * Hoofdtekst van e-mail: *20ffCollectionEmail.html*
   3. Wacht twee dagen nadat u de hierboven vermelde e-mailberichten hebt verzonden
   4. Als het beoogde e-mailbericht niet binnen 2 dagen wordt geopend, verzendt u de **Luminantie - 20 %off e-mail verzameling** als laatste poging tot heroriënteren


>[!TAB Succescriteria]

#### E-mails voorvertonen

**E-mailbericht #1 - Luma - Aankondiging van de zomerverzameling**

E-mailvoorvertoning weergeven:

1. Voeg een testprofiel toe: Louise Petti:
   1. Naamruimte: *Luma CRM-id*
   2. Identiteitswaarde: *d1f132f9f9502bba047a6ec86c4b61f9*

Resultaat:
* De onderwerpregel moet als volgt luiden: Louise, de nieuwe collectie Luma is hier!
* De hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien: [Nieuwe aankondiging van verzameling in seizoensinvloeden](/help/challenges/assets/email-assets/SeasonalCollectionEmail.html)


**E-mailbericht nr. 2 - Verzameling van Luma Men**

Een proefdruk naar uzelf sturen:

1. Voeg een testprofiel toe: Stanleigh Stooke:
   1. Naamruimte: *Luma CRM-id*
   1. Identiteitswaarde: `4f34057d9d9e792c28ba18ecae378e98`
1. Selecteer het testprofiel: Stanleigh Stooke
1. Een proefdruk naar uzelf sturen

Resultaat:\
Je ontvangt een e-mail. De onderwerpregel moet &#39;Stanleigh, verken Men&#39;s nieuwe atletische uitrusting!&#39; en de hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien: [Luma Men&#39;s Collection](/help/challenges/assets/email-assets/MensCollectionEmail.html)

>[!NOTE]
>Het kan een paar minuten duren voordat je de proefdruk ontvangt.

**E-mailbericht nr. 3 - Vrouwencollectie Luma**

Geef een voorvertoning van de e-mail weer met het testprofiel &#39;Louise Petti&#39;.

* De onderwerpregel moet als volgt luiden: *Louise, verken Luma&#39;s Women Collection!*
* De hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien: [Luma Women&#39;s Collection](/help/challenges/assets/email-assets/WomensCollectionEmail.html)


**E-mailbericht nr. 4 - Luma 20 % korting op collectie**

Geef een voorvertoning van de e-mail weer met het testprofiel &#39;Louise Petti&#39;.

* De onderwerpregel moet als volgt luiden: *Louise, geniet van 20% korting op de verkoop!*
* De hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien: [Luminantie 20 % korting op collectie](/help/challenges/assets/email-assets/20OOffCollectionEmail.html)


#### Uw reis testen

>[!IMPORTANT]
>
>Voordat u de overgang naar de testmodus instelt:
>
>1. Zorg ervoor dat voor de activiteit Leessegment de naamruimte is ingesteld op **Luma CRM-id (lumaCrmId)**
>1. Overschrijf voor elke e-mail de standaard e-mailparameters voor de e-mail, zodat deze naar uw e-mailadres worden verzonden:
   >    * Verborgen waarden weergeven door op het oogsymbool te klikken.
   >    * Klik in de parameters E-mail op het T-symbool (parameteroverschrijving inschakelen)

      >
      >      ![E-mailparameters overschrijven](/help/challenges/assets/c3-override-email-paramters.jpg)
   > 
   >    * Klik in het veld Adres
   >    * Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: `"yourname@yourdomain"` in de uitdrukkingsredacteur en klik o.k.

>


Test de reis en stuur de e-mails naar je eigen account:

1. Het traject in testmodus zetten
2. Eén profiel tegelijk selecteren
3. Wacht tijd: Stel de timer in op 120 seconden (typ deze in het veld).
4. Invoer van triggerprofiel
5. U kunt elke vertakking testen met een van de volgende opties *Luma CRM-id&#39;s* als profiel-id&#39;s:
   * Vrouwelijk: Leora Dietsche, Identiteitswaarde:`a8f14eab3b483c2b96171b575ecd90b1`
   * Mannelijk: Stanleigh Stooke, identiteitswaarde: `4f34057d9d9e792c28ba18ecae378e98`
   * Geslacht niet gespecificeerd: Louise Petti, identiteitswaarde: &quot;d1f132f9f9502bba047a6ec86c4b61f9&quot;

6. Nadat u de profielingang hebt geactiveerd, ontvangt u de eerste e-mail. De koptekst moet worden aangepast aan het profiel dat u hebt gekozen.
7. De reis zou in de respectieve tak moeten verdergaan en u zou de verwante e-mail moeten ontvangen (bijvoorbeeld, als u Wenen kiest, zou u de &quot;Verzameling van de Vrouwen van de Luma&quot;e-mail moeten ontvangen).
8. De tweede e-mail openen en de reis moet worden beëindigd
9. U kunt stap 4 herhalen. - 7. voor alle drie de profielen om te controleren of al uw takken correct werken.
10. Als u de time-outs wilt testen, stelt u de wachttijd in op 30 seconden en activeert u de invoer opnieuw.
11. Open de e-mails die u ontvangt niet (bekijk geen voorbeeld van de e-mail (!) en laat de wachttijd over.

Je ontvangt de volgende e-mails:

* Luma - Nieuwe aankondiging van seizoensverzameling
* Afhankelijk van het testprofiel dat u hebt gebruikt, ontvangt u een van de volgende e-mails:
   * Leora: Luma Women&#39;s Collection
   * Stanleigh: Luma Men&#39;s Collection
   * Louise: Luminantie - 20% korting op verzameling
* Als u het tweede e-mailbericht niet hebt geopend: De luminantie - 20% korting van collectie

>[!TAB Uw werk controleren]

Zo ziet uw reis eruit:

![Reis](/help/challenges/assets/c3-j1-journey.png)

**Voorwaarde - Controlegroep:**

![Controlegroep](/help/challenges/assets/c3-j1-condition-control-group.png)

**Voorwaarde - Geslacht:**\

![Voorwaarde - geslacht](/help/challenges/assets/c3-j1-condition-gender.png)
>[!ENDTABS]
