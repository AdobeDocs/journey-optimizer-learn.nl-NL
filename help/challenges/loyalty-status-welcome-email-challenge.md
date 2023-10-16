---
title: Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging
description: Bouw een reis die automatisch een welkome e e-mail naar klanten verzendt wanneer zij loyaliteitsrij bereiken.
jira: KT-8109
feature: Journeys
role: User
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 7861e0ca17a616273f5ea1b4d850310f1f4ec8b8
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging

| Uitdaging | Een welkome-mail met een status van loyaliteit maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[Segmenten maken](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html)</li> <li>[Segmentkwalificatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-read-segment-qualification.html)</li><li>[HTML-inhoud importeren](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html)</li></ul> |
| Te downloaden middelen | [StatusUpgradeEmail.zip](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

{style="table-layout:auto"}

## Het artikel

Luma biedt een loyaliteitsprogramma als een manier om hun klanten aan te trekken en te behouden. Het programma biedt vier verschillende lagen: Bronze, zilver, goud en platina. Elke loyaliteitslaag ontvangt verschillende beloningen, kortingen, en andere speciale prikkels als beloning voor hun herhaalde zaken.

Om de speciale platina status te onderstrepen, wil Luma een welkome e-mail naar klanten verzenden wanneer zij de platina rij bereiken.

## Uw uitdaging

U bent gevraagd om een reis op te zetten die automatisch een welkome e-mail naar klanten verzendt wanneer zij de platina loyaliteitslaag bereiken.

>[!BEGINTABS]

>[!TAB Taak]

Wanneer een loyaliteitsklant voor de platina tier kwalificeert, zouden zij een e-mail moeten ontvangen om hen van hun nieuwe voordelen te feliciteren en te informeren. Het creatieve team heeft een HTML-bestand geleverd **[Luma - statusupgrade - welkomstmail](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** met de e-mailhoofdtekst.

1. Een [!UICONTROL segment] in Journey Optimizer `Luma - platinum status`.

1. Een reis maken die `Luma - New Status - platinum`.

   1. Een klant beweegt zich in de reis wanneer zij voor de platina loyaliteitslaag in aanmerking komen.

   1. De klant moet een e-mailbericht ontvangen met het label `Luma - Platinum Status - Welcome`, met de onderwerpregel `Welcome to Platinum Status, {firstName}!` via e-mail van het creatieve team. Dit is een [!UICONTROL transactie] e-mail.

   1. Wanneer u het HTML-bestand uploadt, ziet u dat het e-mailbericht verwijst naar de status &#39;ruit&#39; in plaats van naar &#39;platina&#39;. Werk de e-mail in de [!UICONTROL E-mailDesigner].

>[!TAB Succescriteria]

Test uw reis:

1. Zorg ervoor dat de [!UICONTROL Segmentactiviteit lezen] heeft de [!UICONTROL namespace] instellen op **[!DNL Luma CRM id(lumaCrmId)]**.

1. De standaardinstelling overschrijven [!UICONTROL e-mailparameters] en stel het in op uw eigen e-mailadres:
   * In de **[!UICONTROL E-mailparameters]**, klikt u op het T-symbool (parameteroverschrijving inschakelen)

   * Klik op de knop **[!UICONTROL Adres]** veld.

   * Voeg uw e-mailadres tussen haakjes toe op het volgende scherm: `"yourname@yourdomain"` in de uitdrukkingsredacteur, dan klik **[!UICONTROL OK]**.

1. Stel het pad in op de testmodus.

1. Selecteren **[!UICONTROL Een gebeurtenis activeren]**.

1. Voeg het volgende toe `CRM ID` for `Stanleigh Stooke` in de **[!UICONTROL Profiel-id]** veld: `4f34057d9d9e792c28ba18ecae378e98`

**Resultaat** U moet de gepersonaliseerde *Luma - platina Status - Welkom* e-mail.

Zo ziet de e-mail eruit:

![Luma - statusupgrade - welkomstmail](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!TAB Uw werk controleren]

Zo ziet het segment eruit:

![Luma - platina status - segment](/help/challenges/assets/segment-luma-platinum-status.png)

Zo ziet uw reis eruit:

![platina-status-upgrade-reis](/help/challenges/assets/journey-luma-status-upgrade.png)

>[!ENDTABS]
