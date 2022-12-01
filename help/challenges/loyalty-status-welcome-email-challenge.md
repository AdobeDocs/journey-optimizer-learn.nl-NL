---
title: Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging
description: Begrijp de grondbeginselen van het samenstellen van een journey in het journeycanvas.
kt: 8109
feature: Journeys
role: User
level: Beginner
hide: true
exl-id: 6fd58b8e-7178-495d-a85d-eb67fc4f3acf
source-git-commit: bcd4e8f01ebb83444934d641d3ee3aafe420bd6b
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Een welkomstbericht voor een loyaliteitsstatus maken - Uitdaging

![AJO Loyalty-status welkomstmail - Uitdagingsbanner](/help/challenges/assets/email-assets/luma-transactional-onboarding-1.png)

| Uitdaging | Een welkome-mail met een status van loyaliteit maken |
|---|---|
| Persona | Reismanager |
| Vereiste vaardigheden | <ul><li>[E-mailcontent maken met de berichteneditor](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-messages/create-email-content-with-the-message-editor.html?lang=en)</li> <li>[Contextuele gebeurtenisinformatie gebruiken voor personalisatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-contextual-event-information-for-personalization.html?lang=en)</li><li>[Helpfuncties gebruiken voor personalisatie](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/personalize-content/use-helper-functions-for-personalization.html?lang=en)</li></ul> |
| Te downloaden middelen | [Bevestigingsmiddelen bestellen](/help/challenges/assets/email-assets/order-confirmation-assets.zip) |

## Het artikel

Luma biedt een loyaliteitsprogramma als een manier om hun klanten aan te trekken en te behouden. Het programma kent vier verschillende niveaus: Zilver, goud, platina en diamant.

Elke loyaliteitslaag ontvangt verschillende niveaus of beloningen, kortingen, en andere speciale prikkels als beloning voor hun herhaalde zaken.

De speciale diamantstatus onderstrepen. Luma wil een welkome e-mail naar klanten sturen wanneer ze de diamantlijst bereiken.

## Uw uitdaging

U bent opgedragen een reis op te zetten die automatisch een welkome e-mail naar klanten stuurt wanneer zij de diamantloyaliteitslaag bereiken.

>[!NOTE]
> Als u in een gedeelde trainingssandbox werkt, kunt u het beste uw naam of initialen als voorvoegsel toevoegen aan de naam van een element dat u maakt.

>[!BEGINTABS]

>[!TAB Taak]

Stuur een e-mail wanneer een klant van de loyaliteit naar een Ruitvormige rij gaat om hen te feliciteren en van hun nieuwe voordelen op de hoogte te brengen. De

1. Een segment maken met de naam Journey Optimizer **Luma, toestand Ruitvormig**
2. Creeer een reis teweeggebracht wanneer een klant zich in Diamond nieuwe loyaliteitsrij (specifiek wanneer de klant het segment ingaat dat voor een nieuw Ruitvormig lid wordt bepaald) om &quot;Luma - Nieuwe Status - Ruitje - Transactionele&quot;e-mail te verzenden
   1. Een transactie-e-mailbericht maken met de naam `(your name)_Luma – New Status – Diamond – Transactional email message`.
   2. E-mail een onderwerpregel geven `Welcome to Diamond Status, (recipient's first name)!`.
   3. Het opgegeven HTML-bestand gebruiken **[DiamondStatusEmail.html](/help/challenges/assets/email-assets/DiamondStatusEmail.html)** voor de e-mailhoofdtekst.
3. Nadat de reis is voltooid, wordt deze in de testmodus gezet en wordt de reis gestart om naar uzelf te sturen  

   1. Een transactie-e-mailbericht maken met de naam `(your name)_Luma – New Status – Diamond – Transactional email message`.
   1. E-mail een onderwerpregel geven `Welcome to Diamond Status, (recipient's first name)!`.
   1. Het opgegeven HTML-bestand gebruiken **[DiamondStatusEmail.html](/help/challenges/assets/email-assets/DiamondStatusEmail.html)** voor de e-mailhoofdtekst.
4. Nadat de reis is voltooid, wordt deze in de testmodus gezet en wordt de reis gestart om naar uzelf te sturen  

### Luma maken - Nieuwe status - Ruitje - Transactiee-mailbericht

Een welkomstbericht maken

### **Reis nr. 3 - Ruitvormige statusupgrade - e-mail ontvangen**


>[!TAB Succescriteria]

Test uw reis:

1. Zorg ervoor dat de segmentkwalificatiegebeurtenis Namespace = Email heeft
1. Hef de standaard e-mailparameters op en stel deze in op uw eigen e-mailadres
1. De overgang naar de testmodus instellen
1. Een gebeurtenis activeren
1. Voeg het volgende e-mailadres toe aan het veld Profiel-id: Jenna_Palmer9530@emailsim.io

U moet de persoonlijke e-mail &quot;Luma - New Status - Diamond-Transaction&quot; ontvangen.

>[!TAB Uw werk controleren]

Zo ziet uw reis eruit:

![Ruitvormige status-upgrade-reis](/help/challenges/assets/journey-luma-diamond-status-upgrade.png)

>[!ENDTABS]
