---
title: Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging
description: Begrijp de grondbeginselen van het samenstellen van een journey in het journeycanvas.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 27139d8f3b7fc5d6bb2a862789116f5e1f911766
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 3%

---

# Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging

![Loyalty status welkomstmail - Uitdagingsbanner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

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

1. Een [!UICONTROL segment] in Journey Optimizer `Luma – status upgrade`.
2. Een reis maken met de naam `Luma – New Status – platinum`.
   1. Een klant beweegt zich in de reis, wanneer zij voor de platina loyaliteitslaag in aanmerking komen.
   2. De klant moet een e-mailbericht ontvangen met het label `Luma – Platinum Status - Welcome`, met de onderwerpregel `Welcome to Platinum Status, (recipient's first name)!` via e-mail van het creatieve team.
   3. Wanneer u het HTML-bestand uploadt, ziet u dat het e-mailbericht verwijst naar de status &#39;ruit&#39; in plaats van naar &#39;platina&#39;. Werk de e-mail bij in de e-mailontwerper in plaats van een nieuw bestand aan te vragen bij het creatieve team.

>[TIP!]
> Controleer of de Luma - Platinum Status - Welkom e-mail is[!UICONTROL transactie].


>[!TAB Succescriteria]

Test uw reis:

1. Zorg ervoor dat de [!UICONTROL Segmentactiviteit lezen] de [!UICONTROL namespace] instellen op **[!DNL Luma CRM id(lumaCrmId)]**
2. De standaardinstelling overschrijven [!UICONTROL e-mailparameters] en stel het in op uw eigen e-mailadres

+++Klik hier voor meer informatie over het overschrijven van de [!UICONTROL-e-mailparameters].

* Verborgen waarden weergeven door op het oogsymbool te klikken.
* In de [!UICONTROL E-mailparameters], klikt u op het T-symbool (parameteroverschrijving inschakelen)

![E-mailparameters overschrijven](/help/challenges/assets/c3-override-email-paramters.jpg)

* Klik in de [!UICONTROL Adresveld]
* Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: `"yourname@yourdomain"` in de uitdrukkingsredacteur en klik o.k.
+++

1. De overgang naar de testmodus instellen
2. Een gebeurtenis activeren
3. Voeg het volgende toe [!DNL CRM ID] for [!DNL Stanleigh Stooke] in de [!UICONTROL Profiel-id] veld: `4f34057d9d9e792c28ba18ecae378e98`

U moet de gepersonaliseerde *Luma - platina Status - Welkom* e-mail.

>[!TAB Uw werk controleren]

Zo ziet uw reis eruit:

![platina-status-upgrade-reis](/help/challenges/assets/journey-luma-status-upgrade.png)


Zo ziet de e-mail eruit:

![Luma - statusupgrade - welkomstmail](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!ENDTABS]
