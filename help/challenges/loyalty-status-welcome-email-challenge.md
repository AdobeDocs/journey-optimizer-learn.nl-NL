---
title: Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging
description: Begrijp de grondbeginselen van het samenstellen van een journey in het journeycanvas.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 2bddc86066f265cda1d2063db8eb37c9f211eb76
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 3%

---

# Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging

![Loyalty status welkomstmail - Uitdagingsbanner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Uitdaging | Een welkome-mail met een status van loyaliteit maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[Segmenten maken](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html)</li> <li>[Segmentkwalificatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html)</li><li>[HTML-inhoud importeren](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-emails/import-and-author-html-email-content.html)</li></ul> |
| Te downloaden middelen | [StatusUpgradeEmail.zip](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

## Het artikel

Luma biedt een loyaliteitsprogramma als een manier om hun klanten aan te trekken en te behouden. Het programma heeft vier verschillende niveaus: Brons, zilver, goud en platina. Elke loyaliteitslaag ontvangt verschillende beloningen, kortingen, en andere speciale prikkels als beloning voor hun herhaalde zaken.

De speciale platina-status onderstrepen. Luma wil een welkome e-mail naar klanten sturen wanneer ze de platinumlaag bereiken.

## Uw uitdaging

U bent gevraagd om een reis op te zetten die automatisch een welkome e-mail naar klanten verzendt wanneer zij de platina loyaliteitslaag bereiken.

>[!BEGINTABS]

>[!TAB Taak]

Wanneer een loyaliteitsklant voor de platina tier kwalificeert, zouden zij een e-mail moeten ontvangen om hen van hun nieuwe voordelen te feliciteren en te informeren. Het creatieve team heeft een HTML-bestand geleverd **[Luma - statusupgrade - welkomstmail](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** met de e-mailhoofdtekst.

1. Een [!UICONTROL segment] in Journey Optimizer `Luma – platinum status`.
2. Een reis maken met de naam `Luma – New Status – platinum`.
   1. Een klant beweegt zich in de reis, wanneer zij voor de platina loyaliteitslaag in aanmerking komen.
   2. De klant moet een e-mailbericht ontvangen met het label `Luma – Platinum Status - Welcome`, met de onderwerpregel `Welcome to Platinum Status, {firstName}!` via e-mail van het creatieve team. Dit is een [!UICONTROL transactie] e-mail.
   3. Wanneer u het HTML-bestand uploadt, ziet u dat het e-mailbericht verwijst naar de status &#39;ruit&#39; in plaats van naar &#39;platina&#39;. Werk de e-mail in de [!UICONTROL e-mailontwerper].

>[!TAB Succescriteria]

Test uw reis:

1. Zorg ervoor dat de [!UICONTROL Segmentactiviteit lezen] de [!UICONTROL namespace] instellen op **[!DNL Luma CRM id(lumaCrmId)]**
2. De standaardinstelling overschrijven [!UICONTROL e-mailparameters] en stel het in op uw eigen e-mailadres
   * In de [!UICONTROL E-mailparameters], klikt u op het T-symbool (parameteroverschrijving inschakelen)
   * Klik in de [!UICONTROL Adresveld]
   * Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: `"yourname@yourdomain"` in de uitdrukkingsredacteur en klik o.k.
3. De overgang naar de testmodus instellen
4. Selecteren **Een gebeurtenis activeren**
5. Voeg het volgende toe [!DNL CRM ID] for `Stanleigh Stooke` in de [!UICONTROL Profiel-id] veld: `4f34057d9d9e792c28ba18ecae378e98`

**Resultaat:** U moet de gepersonaliseerde *Luma - platina Status - Welkom* e-mail.

Zo ziet de e-mail eruit:

![Luma - statusupgrade - welkomstmail](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!TAB Uw werk controleren]

Zo ziet het segment eruit:

![Luma - platina status - segment](/)

Zo ziet uw reis eruit:

![platina-status-upgrade-reis](/help/challenges/assets/journey-luma-status-upgrade.png)

>[!ENDTABS]
