---
title: Aankondiging van een zomerverzameling maken - uitdaging
description: Verzend een aankondiging van de Inzameling van de Zomer naar een segment van bestaande klanten om de nieuwe Inzameling van de Zomer van de Luma te bevorderen.
jira: KT-8109
role: User
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: ae457be7-2c67-4950-a072-1d7030b0e17b
source-git-commit: 81f5cc22d46f89ee1c7164a92988311ca6036b8b
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 1%

---

# Aankondiging van een zomerverzameling maken - uitdaging

![Aankondigingsbanner voor AJO Summer Collection](/help/challenges/assets/email-assets/luma-transactional-onboarding-3.png)

| Uitdaging | Een mededeling voor een zomerverzameling maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[Segmenten maken](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html?lang=en)</li><li> [HTML-e-mailcontent importeren en opstellen](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html?lang=en)</li><li>[Gebruiksscenario - Leessegment](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment.html?lang=en)</li> |
| Te downloaden middelen | [E-mailbestanden voor seizoensgebonden verzameling](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip) |

{style="table-layout:auto"}

## Het artikel

Luma, een fictioneel atletisch kledingbedrijf, promoot zijn nieuwste kleding en tandwielcollectie en drijft de verkoop voor bestaande klanten aan. Luma lanceert de nieuwe Inzameling van de Zomer en zou verschillende klantensegmenten specifiek willen richten.

## Uw uitdaging

Het marketingteam van Luma vraagt u om een marketingcampagne voor Summer Collection in Journey Optimizer uit te voeren. Uw uitdaging is:

* Maak een segment waarin wordt gedefinieerd welke profielen in aanmerking komen om de speciale actie te ontvangen.
* Bouw de reis.

### Stap 1: Bepaal het segment - Actieve Klanten

>[!BEGINTABS]

>[!TAB Taak]

#### Een segment maken in [!DNL Journey Optimizer]

* Een segment maken in [!DNL Journey Optimizer] gebeld *Actieve klanten*.
* Het segment moet alleen actieve Luma-klanten bevatten.
* Actieve klanten worden gedefinieerd als klanten met een laag in het loyaliteitsprogramma van Luma (bronze, zilver, goud of platina).


>[!TAB Succescriteria]

In de segmentbouwer, kunt u het geschatte aantal gekwalificeerde profielen zien. Als u met de gegevens van de trainingssandbox werkt, hebt u ongeveer 753 gekwalificeerde profielen van 1,29 kB.

>[!NOTE]
>Het kan tot 24 uren duren voor het segmentlidmaatschap voor bestaande profielen verschijnt, aangezien de bestaande profielen moeten worden teruggevuld.

**Er is een in aanmerking komend profiel toegevoegd aan het segment:**

U kunt controleren de profielen die aan het segment zijn toegevoegd kwalificeren door aan één van in de profielen te navigeren die op de de detailmening van uw segment worden vermeld.

Controleer op de profielpagina de [!UICONTROL Attributen] om te bevestigen dat zij in aanmerking komen: De laag moet zilver, goud, platina of diamant zijn.

![Profielkenmerken](assets/C1-S1-profile-attributes.png)

U kunt ook de [!UICONTROL Segmentlidmaatschap] tab: Uw segment moet worden vermeld.

![Segmentlidmaatschap](assets/C1-S1-profile-segment-membership.png)

>[!TAB Uw werk controleren]

Segmentvelden: **[!UICONTROL Attributen]** > **[!UICONTROL Afzonderlijk XDM-profiel]** > **[!UICONTROL Loyalty]** > **[!UICONTROL Tier]**

Zo ziet uw segment eruit:

![Segment - Actieve klanten](/help/challenges/assets/C1-S1.png)

De code moet er als volgt uitzien:

```javascript
stringCompare("equals", loyalty.tier, ["diamond", "gold", "platinum", "silver"], false)
```

>[!ENDTABS]


### Stap 2: Aankondiging Reis - zomerverzameling maken

>[!BEGINTABS]

>[!TAB Taak]

#### De aankondiging van de zomerverzameling verzenden

Een bureau heeft u vier HTML-bestanden geleverd met het ontwerp voor de e-mails:

* `SeasonalCollectionEmail.html`
* E-mail verzameling Luma Men&#39;s
* E-mail over verzameling van vrouwen in de luminantie
* Luminantie - 20 % korting op e-mail verzameling

1. [De e-mailbestanden voor seizoensverzamelingen downloaden](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip).

1. Een reis maken met de naam *Aankondiging van Luma-zomerverzameling* op basis van de volgende richtsnoeren :

   1. Verzenden *Luma - Nieuwe mededeling over de zomerverzameling* e-mailen naar *Actieve klanten* segment, dat 10% van het publiek als controlegroep uithoudt
      * Berichttitel *Luma - Aankondiging zomerverzameling*
      * Onderwerpregel *(de voornaam van de ontvanger), is de nieuwe inzameling van de Zomer Luma hier!*
      * Het opgegeven HTML-bestand gebruiken `SeasonalCollectionEmail.html` voor de e-mailhoofdtekst.
   1. Wacht twee dagen en verzend een vervolgbericht met meer gerichte inhoud:
      * Mannelijke klanten moeten de **Luma Men&#39;s Collection** e-mail.
         * Berichttitel: *Luma Men&#39;s Collection*
         * Onderwerpregel: *(voornaam van de ontvanger), verken Men&#39;s nieuwe atletische uitrusting!*
         * Hoofdtekst van e-mail: `MensCollectionEmail.html` voor de e-mailhoofdtekst.
      * Vrouwelijke klanten moeten de **Luma Women&#39;s Collection** e-mail.
         * Berichttitel: *Luma Women&#39;s Collection*
         * Onderwerpregel: *(voornaam van ontvanger), ontdek Luma&#39;s Women Collection!*
         * Hoofdtekst van e-mail: `WomensCollectionEmail.html`
      * Andere klanten moeten de **Luma - 20 % korting op collectie** e-mail.
      * Berichttitel: *Luma - 20 % korting op collectie*
      * Onderwerpregel: *(voornaam van ontvanger), geniet van 20% korting op de verkoop!*
      * Hoofdtekst van e-mail: `20OOffCollectionEmail.html`
   1. Wacht twee dagen nadat u de hierboven vermelde e-mailberichten hebt verzonden
   1. Als het beoogde e-mailbericht niet binnen 2 dagen wordt geopend, verzendt u de **Luminantie - 20 %off e-mail verzameling** als laatste poging tot heroriënteren


>[!TAB Succescriteria]

#### E-mails voorvertonen

**E-mailbericht #1 - Luma - Aankondiging van de zomerverzameling**

E-mailvoorvertoning weergeven:

1. Voeg een testprofiel toe: Louise Petti:
   * Naamruimte: *Luma CRM-id*
   * Identiteitswaarde: *d1f132f9f9502bba047a6ec86c4b61f9*

Resultaat:

* De onderwerpregel moet als volgt luiden: Louise, de nieuwe collectie Luma is hier!

**E-mailbericht nr. 2 - Verzameling van Luma Men**

Een proefdruk naar uzelf sturen:

1. Voeg een testprofiel toe: Stanleigh Stooke:
   * Naamruimte: *Luma CRM-id*
   * Identiteitswaarde: `4f34057d9d9e792c28ba18ecae378e98`
2. Selecteer het testprofiel: Stanleigh Stooke.
3. Stuur een proef naar uzelf.

Resultaat:\
Je ontvangt een e-mail. De onderwerpregel moet *Stanleigh, ontdek de nieuwe atletische uitrusting van Men!* en de hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien.

>[!NOTE]
>Het kan een paar minuten duren voordat je de proefdruk ontvangt.

**E-mailbericht #3 - Luma Women&#39;s Collection**

E-mail voorvertonen met het testprofiel *Louise Petti.*

* De onderwerpregel moet als volgt luiden: *Louise, verken Luma&#39;s Women Collection!*

**E-mailbericht #4 - Luma 20 % korting op collectie**

E-mail voorvertonen met het testprofiel *Louise Petti.*

* De onderwerpregel moet als volgt luiden: *Louise, geniet van 20% korting op de verkoop!*

#### Uw reis testen

>[!IMPORTANT]
>
>Voordat u de overgang naar de testmodus instelt:
>
>1. Zorg ervoor dat de [!UICONTROL Segmentactiviteit lezen] heeft de naamruimte ingesteld op **Luma CRM-id (lumaCrmId)**
>1. Overschrijf voor elke e-mail de standaard e-mailparameters voor de e-mail, zodat deze naar uw e-mailadres worden verzonden:
>    * Verborgen waarden weergeven door op het oogsymbool te klikken.
>    * Klik in de e-mailparameters op het T-symbool (parameteroverschrijving inschakelen).
>
>      ![E-mailparameters overschrijven](/help/challenges/assets/c3-override-email-paramters.jpg)
> 
>    * Klik in de [!UICONTROL Adres] field
>    * Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: `"yourname@yourdomain"` in de uitdrukkingsredacteur en klik o.k.
>

Test de reis en stuur de e-mails naar je eigen account:

1. Zet de reis in testmodus.
1. Selecteren **[!UICONTROL Eén profiel tegelijk]**.
1. Wacht tijd: Stel de timer in op 120 seconden (typ deze in het veld).
1. Invoer van triggerprofiel
1. U kunt elke vertakking testen met een van de volgende opties *Luma CRM-id&#39;s* als profiel-id&#39;s:
   * Vrouwelijk: Leora Dietsche, Identiteitswaarde:`a8f14eab3b483c2b96171b575ecd90b1`
   * Mannelijk: Stanleigh Stooke, identiteitswaarde: `4f34057d9d9e792c28ba18ecae378e98`
   * Geslacht niet gespecificeerd: Louise Petti, identiteitswaarde: `d1f132f9f9502bba047a6ec86c4b61f9`

1. Nadat u de profielingang teweegbrengt, zou u eerste e-mail moeten ontvangen. De koptekst moet worden aangepast aan het profiel dat u hebt gekozen.
1. De reis zou in de respectieve tak moeten verdergaan, en u zou verwante e-mail moeten ontvangen (bijvoorbeeld als u verkoos *Jenna*, moet u de *Luma Women&#39;s Collection* e-mail).
1. Open de tweede e-mail en de reis moet worden beëindigd.
1. U kunt stap 4 herhalen. - 7. voor alle drie de profielen om te controleren of uw takken correct werken.
1. Als u de time-outs wilt testen, stelt u de wachttijd in op 30 seconden en activeert u de invoer opnieuw.
1. Open de e-mails die u ontvangt niet (bekijk geen voorbeeld van de e-mail (!) en laat de wachttijd over.

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
