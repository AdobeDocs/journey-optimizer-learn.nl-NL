---
title: Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging
description: Bouw een reis die automatisch een welkome e e-mail naar klanten verzendt wanneer zij loyaliteitsrij bereiken.
jira: KT-8109
feature: Journeys
role: User
level: Beginner
last-substantial-update: 2023-02-01T00:00:00Z
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: 201470e35095b38617d1a1bb5d7b16c1e60f431e
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging

| Uitdaging | Een welkome-mail met een status van loyaliteit maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[ creeer segmenten ](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/profiles-segments-subscriptions/create-segments.html)</li> <li>[ kwalificatie van het Segment ](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journeys/use-case-read-segment-qualification.html)</li><li>[ de inhoud van HTML van de Invoer ](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/import-and-author-html-email-content.html)</li></ul> |
| Assets downloaden | [ StatusUpgradeEmail.zip ](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip) |

{style="table-layout:auto"}

## Het artikel

Luma biedt een loyaliteitsprogramma als een manier om hun klanten aan te trekken en te behouden. Het programma biedt vier verschillende lagen: Bronze, zilver, goud en platina. Elke loyaliteitslaag ontvangt verschillende beloningen, kortingen, en andere speciale prikkels als beloning voor hun herhaalde zaken.

Om de speciale platina status te onderstrepen, wil Luma een welkome e-mail naar klanten verzenden wanneer zij de platina rij bereiken.

## Uw uitdaging

U bent gevraagd om een reis op te zetten die automatisch een welkome e-mail naar klanten verzendt wanneer zij de platina loyaliteitslaag bereiken.

>[!BEGINTABS]

>[!TAB Taak]

Wanneer een loyaliteitsklant voor de platina tier kwalificeert, zouden zij een e-mail moeten ontvangen om hen van hun nieuwe voordelen te feliciteren en te informeren. Het creatieve team heeft een dossier van HTML **[Luma - statusverbetering verstrekt - verwelkom e-mail](/help/challenges/assets/email-assets/StatusUpgradeEmail.zip)** met het e-maillichaam.

1. Creeer geroepen a [!UICONTROL  segment ] in Journey Optimizer `Luma - platinum status`.

1. Maak een reis met de naam `Luma - New Status - platinum` .

   1. Een klant beweegt zich in de reis wanneer zij voor de platina loyaliteitslaag in aanmerking komen.

   1. De klant dient een e-mailbericht met het label `Luma - Platinum Status - Welcome` te ontvangen, met de onderwerpregel `Welcome to Platinum Status, {firstName}!` en de e-mailtekst die door het creatieve team is verschaft. Dit is a [!UICONTROL  transactie ] e-mail.

   1. Wanneer u het HTML-bestand uploadt, verwijst het e-mailbericht naar de status &#39;ruit&#39; in plaats van naar &#39;platina&#39;. In plaats van het verzoeken van om een nieuw dossier van het creatieve team, werk e-mail in [!UICONTROL  E-mail Designer ] bij.

>[!TAB  criteria van het Succes ]

Test uw reis:

1. Zorg ervoor dat de [!UICONTROL  Gelezen Activiteit van het Segment ] [!UICONTROL  namespace ] heeft die aan **[!DNL Luma CRM id(lumaCrmId)]** wordt geplaatst.

1. Overschrijf de standaard [!UICONTROL  e-mailparameters ] en plaats het aan uw eigen e-mailadres:
   * In de **[!UICONTROL parameters E-mail]**, klik het T symbool (laat parameteropheffing toe)

   * Klik het **[!UICONTROL gebied van het Adres]**.

   * Op het volgende scherm, voeg uw e-mailadres tussen haakjes toe: `"yourname@yourdomain"` in de uitdrukkingsredacteur, dan klik O.K. ****.

1. Stel het pad in op de testmodus.

1. Selecteer **[!UICONTROL Trigger een gebeurtenis]**.

1. Voeg het volgende `CRM ID` voor `Stanleigh Stooke` op het **[!UICONTROL Herkenningsteken van het Profiel]** gebied toe: `4f34057d9d9e792c28ba18ecae378e98`

**Resultaat:** u zou gepersonaliseerde *Luma - platinaStatus - Welkome* e-mail moeten ontvangen.

Zo ziet de e-mail eruit:

![ Luma - statusverbetering - verwelkom e-mail ](/help/challenges/assets/status-upgrade-welcome-email.png)

>[!TAB  Controle uw werk ]

Zo ziet het segment eruit:

![ Luma - platina status - segment ](/help/challenges/assets/segment-luma-platinum-status.png)

Zo ziet uw reis eruit:

![ platina-status-verbetering-reis ](/help/challenges/assets/journey-luma-status-upgrade.png)

>[!ENDTABS]
