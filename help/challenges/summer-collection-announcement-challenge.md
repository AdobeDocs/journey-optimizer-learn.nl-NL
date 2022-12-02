---
title: Een mededeling over een zomerverzameling maken - Uitdaging
description: Verzend een mededeling van de zomerinzameling aan een segment van bestaande klanten' om de nieuwe inzameling van de zomer van de Luma te bevorderen.
kt: 8109
role: User
level: Beginner
last-substantial-update: 2022-11-16T00:00:00Z
hide: true
exl-id: ae457be7-2c67-4950-a072-1d7030b0e17b
source-git-commit: 697f4e6b11e7c40be726471ab368781f32dad165
workflow-type: tm+mt
source-wordcount: '1138'
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

Het marketingteam van Luma vraagt u om een marketingcampagne voor de zomerverzameling in Journey Optimizer uit te voeren. Je uitdaging is om een reis te maken in Journey Optimizer. Specifiek, moet u het vereiste segment creëren, vier berichten creëren, en de reis bouwen.


### Stap 1: Het segment definiëren - actieve klanten

>[!BEGINTABS]

>[!TAB Taak]

Een segment maken met de naam Journey Optimizer **Actieve klanten**.

* Het segment moet alleen actieve Luma-klanten bevatten.
* Actieve klanten worden gedefinieerd als klanten met een laag in het loyaliteitsprogramma van Luma (zilver, goud, platina of diamant).


>[!TAB Succescriteria]

In de segmentbouwer, kunt u het geschatte aantal gekwalificeerde profielen zien.

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

Verzend een aankondiging van de zomerinzameling naar een segment van bestaande e-mail van klanten die de nieuwe inzameling van de zomer van de Luma promoten. &quot;

Een bureau heeft u vier HTML-bestanden geleverd met het ontwerp voor de e-mails: [De e-mailbestanden voor seizoensverzamelingen downloaden](/help/challenges/assets/email-assets/emails-seasonal-collection-announcement.zip)

Een reis maken met de naam `(your name) - Summer collection announcement` op basis van de volgende richtsnoeren :

1. Verzend Luma - de Nieuwe E-mail van de Aankondiging van de Seizoensgebonden Inzameling naar het Luma-Actieve segment van Klanten, die 10% van het publiek als controlegroep houden
   * Berichttitel `(your name)_Luma New Seasonal Collection Announcement`.
   * Onderwerpregel `(recipient's first name), the new Luma collection is here!`.
   * Het opgegeven HTML-bestand gebruiken *SeasonalCollectionEmail.html* voor de e-mailhoofdtekst.
2. Wacht twee dagen en verzend een vervolgbericht met meer gerichte inhoud:
   * Mannelijke klanten moeten de **E-mail verzameling Luma Men&#39;s**
      * Berichttitel: **(uw naam)_Luma Men&#39;s Collection**
      * Onderwerpregel: **(voornaam van de ontvanger), verken Men&#39;s nieuwe atletische uitrusting!**
      * Hoofdtekst van e-mail: *MensCollectionEmail.html* voor de e-mailhoofdtekst.
   * Vrouwelijke klanten moeten de **E-mail over verzameling van vrouwen in de luminantie**
      * Berichttitel: **(uw naam)_Luma Women&#39;s Collection**
      * Onderwerpregel: **(voornaam van ontvanger), ontdek Luma&#39;s Women Collection!**
      * Hoofdtekst van e-mail: *WomensCollectionEmail.html*
   * Andere klanten moeten de **Luminantie - 20 % korting op e-mail verzameling**
      * Berichttitel: **(uw naam)_Luma - 20 % korting op collectie**
      * Onderwerpregel:**(voornaam van ontvanger), geniet van 20% korting op de verkoop!**
      * Hoofdtekst van e-mail: *20ffCollectionEmail.html*
3. Wacht twee dagen nadat u de hierboven vermelde e-mailberichten hebt verzonden
4. Als het beoogde e-mailbericht niet binnen 2 dagen wordt geopend, verzendt u de **Luminantie - 20 %off e-mail verzameling** als laatste poging tot heroriënteren


>[!TAB Succescriteria]

#### E-mails voorvertonen

**E-mailbericht #1 - Nieuwe aankondiging van verzameling seizoensinvloeden**

Geef een voorbeeld van de e-mail weer met de naamruimte Identiteit: *E-mail* en de identiteitswaarde: *Jenna_Palmer9530@emailsim.io*

* De onderwerpregel moet als volgt luiden: Jenna, de nieuwe collectie Luma is hier!
* De hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien: [Nieuwe aankondiging van verzameling in seizoensinvloeden](/help/challenges/assets/email-assets/SeasonalCollectionEmail.html)


**E-mailbericht nr. 2 - Verzameling van Luma Men**

Een proefdruk naar uzelf sturen

* Voer uw e-mailadres in
* Selecteer het testprofiel: Chris_Scott1244@emailsim.io

Je ontvangt een e-mail. De onderwerpregel zou moeten lezen: &quot;Chris, verken Men&#39;s nieuwe atletische tandwiel!&quot; en de hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien: [Luma Men&#39;s Collection](/help/challenges/assets/email-assets/MensCollectionEmail.html)

**E-mailbericht nr. 3 - Vrouwencollectie Luma**

Geef een voorbeeld van de e-mail weer met de naamruimte Identiteit: *E-mail* en de identiteitswaarde: *Jenna_Palmer9530@emailsim.io*

* De onderwerpregel moet als volgt luiden: *Jenna, verken Luma&#39;s Women Collection!*
* De hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien: [Luma Women&#39;s Collection](/help/challenges/assets/email-assets/WomensCollectionEmail.html)


**E-mailbericht nr. 4 - Luma 20 % korting op collectie**

Geef een voorbeeld van de e-mail weer met de naamruimte Identiteit: *E-mail* en de identiteitswaarde: *Benny_Steer4909@emailsim.io*

* De onderwerpregel moet als volgt luiden: *Benny, geniet van 20% korting op de verkoop!*
* De hoofdtekst van de e-mail moet overeenkomen met wat u in de voorvertoning hebt gezien: [Luminantie 20 % korting op collectie](/help/challenges/assets/email-assets/20OOffCollectionEmail.html)

**Vergeet niet uw e-mails te publiceren!**

#### Uw reis testen

>[!IMPORTANT]
>
>Voordat u de overgang naar de testmodus instelt:
>
>1. Zorg ervoor dat voor de activiteit Leessegment de naamruimte is ingesteld op E-mail
>1. Overschrijf voor elke e-mail de standaard e-mailparameters voor de e-mail, zodat deze naar uw e-mailadres worden verzonden:
>1. Verborgen waarden weergeven door op het oogsymbool te klikken.
>1. Klik in de parameters E-mail op het T-symbool (parameteroverschrijving inschakelen)

   >
   >      ![E-mailparameters overschrijven](/help/challenges/assets/c3-override-email-paramters.jpg)
> 
>1. Klik in het veld Adres
>1. Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: *yourname@yourdomain* in de uitdrukkingsredacteur en klik o.k.

>


Test de reis en stuur de e-mails naar je eigen account:

1. Het traject in testmodus zetten
2. Eén profiel tegelijk selecteren
3. Wacht tijd: Stel de timer in op 120 seconden (typ deze in het veld).
4. Invoer van triggerprofiel
5. U kunt elke vertakking testen door een van de volgende e-mailadressen als profiel-id&#39;s te gebruiken:
   * Vrouwelijk: Jenna Palmer: Jenna_Palmer9530@emailsim.io
   * Mannelijk: Chris Scott: Chris_Scott1244@emailsim.io
   * Geslacht niet gespecificeerd: Benny Steer: Benny_Steer4909@emailsim.io

6. Nadat u de profielingang hebt geactiveerd, ontvangt u de eerste e-mail. De koptekst moet worden aangepast aan het profiel dat u hebt gekozen.
7. De reis zou in de respectieve tak moeten verdergaan en u zou de verwante e-mail moeten ontvangen (bijvoorbeeld, als u Wenen kiest, zou u de &quot;Verzameling van de Vrouwen van de Luma&quot;e-mail moeten ontvangen).
8. De tweede e-mail openen en de reis moet worden beëindigd
9. U kunt stap 4 herhalen. - 7. voor alle drie de profielen om te controleren of al uw takken correct werken.
10. Als u de time-outs wilt testen, stelt u de wachttijd in op 30 seconden en activeert u de invoer opnieuw.
11. Open de e-mails die u ontvangt niet (bekijk geen voorbeeld van de e-mail (!) en laat de wachttijd over.

Je ontvangt de volgende e-mails:

* Luma - Nieuwe aankondiging van seizoensverzameling
* Afhankelijk van het testprofiel dat u hebt gebruikt, ontvangt u een van de volgende e-mails:
   * Wenen: Luma Women&#39;s Collection
   * Chris: Luma Men&#39;s Collection
   * Benny: Luminantie - 20% korting op verzameling
* Als u het tweede e-mailbericht niet hebt geopend: De luminantie - 20% korting van collectie

>[!TAB Uw werk controleren]

Zo ziet uw reis eruit:

![Reis](/help/challenges/assets/c3-j1-journey.png)

**Voorwaarde - Controlegroep:**

![Controlegroep](/help/challenges/assets/c3-j1-condition-control-group.png)

**Voorwaarde - Geslacht:**\

![Voorwaarde - geslacht](/help/challenges/assets/c3-j1-condition-gender.png)
>[!ENDTABS]
