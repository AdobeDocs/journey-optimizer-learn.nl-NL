---
title: Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging
description: Begrijp de grondbeginselen van het samenstellen van een journey in het journeycanvas.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: e148101f8404c8e2019ee17823bcf1d7a9668bc5
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 3%

---

# Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging

![AJO Loyalty-status welkomstmail - Uitdagingsbanner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Uitdaging | Een welkome-mail met een status van loyaliteit maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[Segmenten maken](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html)</li> <li>[Segmentkwalificatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html)</li><li>[HTML-inhoud importeren](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html)</li></ul> |
| Te downloaden middelen | [platinumStatusEmail.zip](/help/challenges/assets/email-assets/platinumStatusEmail.zip) |

## Het artikel

Luma biedt een loyaliteitsprogramma als een manier om hun klanten aan te trekken en te behouden. Het programma kent vier verschillende niveaus: Brons, zilver, goud en platina. Elke loyaliteitslaag ontvangt verschillende niveaus of beloningen, kortingen, en andere speciale prikkels als beloning voor hun herhaalde zaken.

De speciale platina-status onderstrepen. Luma wil een welkome e-mail naar klanten sturen wanneer ze de platinumlaag bereiken.

## Uw uitdaging

U bent gevraagd om een reis op te zetten die automatisch een welkome e-mail naar klanten verzendt wanneer zij de platina loyaliteitslaag bereiken.

>[!BEGINTABS]

>[!TAB Taak]

Wanneer een loyaliteitsklant voor de platina tier in aanmerking komt, zouden zij en e-mail moeten ontvangen om hen van hun nieuwe voordelen te feliciteren en te informeren. Het creatieve team heeft een HTML-bestand geleverd **[Luma - statusupgrade - welkomstmail](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** met de e-mailhoofdtekst.

1. Een segment maken met de naam Journey Optimizer `Luma – status upgrade`.
2. Maak een reis met de naam &#39;Luma - New Status - platinum&#39;.
   1. Een klant beweegt zich in de reis, wanneer zij voor de platina loyaliteitslaag in aanmerking komen.
   2. De klant moet een e-mailbericht ontvangen met het label `Luma – Platinum Status - Welcome`, met de onderwerpregel `Welcome to Platinum Status, (recipient's first name)!` met het lichaam van het creatieve team.
   3. Wanneer u het HTML-bestand uploadt, ziet u dat het e-mailbericht verwijst naar de status &#39;ruit&#39; in plaats van naar &#39;platina&#39;. Werk de e-mail in de e-mailontwerper bij in plaats van een nieuw bestand aan te vragen bij het creatieve team.

>[TIP!]
> Zorg ervoor dat de Luma - Platinum Status - Welkome e-mail transactioneel is.


>[!TAB Succescriteria]

Test uw reis:

1. Zorg ervoor dat voor de activiteit Leessegment de naamruimte is ingesteld op **Luma CRM-id (lumaCrmId)**
2. Hef de standaard e-mailparameters op en stel deze in op uw eigen e-mailadres

+++ Klik hier voor meer informatie over hoe u deze kunt overschrijven
   * Verborgen waarden weergeven door op het oogsymbool te klikken.
   * Klik in de parameters E-mail op het T-symbool (parameteroverschrijving inschakelen)

   ![E-mailparameters overschrijven](/help/challenges/assets/c3-override-email-paramters.jpg)

   * Klik in het veld Adres
   * Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: `"yourname@yourdomain"` in de uitdrukkingsredacteur en klik o.k.
+++


3. De overgang naar de testmodus instellen
4. Een gebeurtenis activeren
5. Voeg de volgende CRM-id voor Standaardlijn toe aan het veld Profiel-id: `4f34057d9d9e792c28ba18ecae378e98`

U moet de gepersonaliseerde *Luma - platina Status - Welkom* e-mail.

>[!TAB Uw werk controleren]

Zo ziet uw reis eruit:

![platina-status-upgrade-reis](/help/challenges/assets/journey-luma-status-upgrade.png)


Zo ziet de e-mail eruit:

![Luma - statusupgrade - welkomstmail](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!ENDTABS]
