---
title: Reizen maken - Uitdaging
description: Begrijp de grondbeginselen van het samenstellen van een journey in het journeycanvas.
kt: 8109
feature: Journeys
role: User
level: Beginner
source-git-commit: e75564c24f79eaecc1384fde978cc81cb2b9bdaf
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 1%

---


# Reizen maken - Uitdaging

## Het artikel

Luma, een fictioneel atletisch kledingbedrijf, wil zijn nieuwste kleding- en tandwielcollectie promoten en de verkoop voor bestaande klanten stimuleren. Het marketingteam van Luma vraagt u een marketingcampagne voor de zomerverzameling en extra gebruiksgevallen te implementeren die de ervaring van de klant verbeteren en het behoud verhogen.

Uw uitdaging is reizen te maken om de volgende gebruiksgevallen te implementeren:

1. Om de nieuwe inzameling van de zomer van de Luma te bevorderen, verzend een mededeling van de zomerinzameling aan een segment van bestaande klanten e-mail
2. Een bevestigingsbericht voor bestellingen verzenden wanneer iemand een online aankoop heeft voltooid
3. Verzend een e-mail wanneer een loyaliteitsklant naar een nieuwe rij beweegt om hen te feliciteren en te informeren over hun nieuwe voordelen
4. Wanneer een eerder uit voorraad bestaand artikel weer in voorraad is, geeft u klanten die het out-of-stock-item hebben bevoordeeld een melding om te gaan winkelen nu het item weer in voorraad is

## UW UITDAGING

De volgende reizen maken in Journey Optimizer:

### **Journaal 1 - Aankondiging van de zomerverzameling**

Om de nieuwe inzameling van de zomer van de Luma te bevorderen, verzend een mededeling van de zomerinzameling aan een segment van bestaande klanten e-mail.

1. Verzend &quot;Luma - de Nieuwe Aankondiging van de Verzameling van de Seizoen&quot;e-mail naar het Actieve segment van de Klant, die 10% van het publiek als controlegroep houdt.
2. Als een ontvanger het dialoogvenster *Luma - Nieuwe aankondiging van seizoensverzameling* Stuur binnen twee dagen een vervolgbericht met meer gerichte inhoud per e-mail:
   * Mannelijke klanten moeten de *Luminantiegzameling - mannen* email
   * Vrouwelijke klanten moeten de *Luminantiegzameling, voor vrouwen* email
   * Andere klanten moeten de *Luma - 20% korting op collectie* email
3. Nadat u de hierboven vermelde e-mails hebt verzonden, wacht u een uur en luistert u naar het openen van de e-mail.
4. Als het beoogde e-mailbericht niet binnen 2 dagen wordt geopend, verzendt u de *Luma - 20% korting op verkoop* e-mailen als laatste poging tot opnieuw richten.
5. Als de reis eenmaal is voltooid, zet deze in de testmodus en zet deze de reis op om naar uzelf te sturen.

SUCCESCRITERIA

Je ontvangt de volgende e-mails:

* *Luma - Nieuwe aankondiging van seizoensverzameling*
* Als u de eerste email: The e-mail met de collectie Luma&#39;s opent voor mannen of vrouwen als u het geslacht hebt toegevoegd, zo niet de Luma 20% korting op de e-mail met de collectie
* Als u het tweede e-mailbericht niet hebt geopend: De *Luma - 20% korting op verkoop* email

### **Reis 2 - Bevestiging van transactie-e-mail**

Stuur een bevestigingsbericht voor bestellingen wanneer iemand een online aankoop heeft voltooid.

>[!INFO]
>
>Als u het [Berichten maken en personaliseren](/help/challenges/create-and-personalize-emails-challenge.md)U kunt deze reis overslaan en naar Reis #3 gaan.

1. Maak een reis die wordt geactiveerd wanneer een klant een internetaankoop op de Luma-site voltooit en het e-mailbericht &quot;Luma - website - bestelling bevestigen&quot; verzendt.
2. Contextuele informatie toewijzen vanuit de *LumaOnlinePurchase* om de e-mail aan te passen. Als u een afbeelding wilt aanpassen aan contextuele informatie, moet u het dialoogvenster *Luma - Website - Bevestiging van de Orde* e-mail en prefix het met uw naam en gebruik dat in de reis.
3. Als de reis eenmaal is voltooid, zet deze in de testmodus en zet deze de reis op om naar uzelf te sturen. U kunt &quot;LLWH06&quot;voor product SKU (de Eenheid van het Houden van de Voorraad) gebruiken wanneer het testrenteren van de testgebeurtenis, of de producten op de [Luma-website](https://publish1034.adobedemo.com/content/luma/us/en.html) als u een ander product wilt kiezen. De SKU staat op elke productpagina, maar laat het achtervoegsel weg dat kleur/grootte, bijvoorbeeld &quot;.1-XS&quot; aanduidt

SUCCESCRITERIA

U ontvangt het bevestigingsbericht voor een persoonlijke aankoop met het opgegeven product.

### **Reis nr. 3 - Ruitvormige statusupgrade - e-mail ontvangen**

Verzend een e-mail wanneer een loyaliteitsklant naar een nieuwe rij beweegt om hen van hun nieuwe voordelen te feliciteren en te informeren.

1. Creeer een reis teweeggebracht wanneer een klant zich in Diamond nieuwe loyaliteitsrij (specifiek wanneer de klant het segment ingaat dat voor een nieuw Ruitvormig lid wordt bepaald) om &quot;Luma - Nieuwe Status - Ruitje - Transactionele&quot;e-mail te verzenden
2. Nadat de reis is voltooid, wordt deze in de testmodus gezet en wordt de reis gestart om naar uzelf te sturen  

SUCCESCRITERIA

U moet de persoonlijke e-mail &quot;Luma - New Status - Diamond-Transaction&quot; ontvangen.

### **Reis nr. 4 - E-mail met productvoorraad**

Wanneer een eerder uit voorraad bestaand item weer in voorraad is, geeft u klanten die het out-of-stock-item hebben bevoordeeld een melding om te gaan winkelen nu het item weer in voorraad is.

1. Maak een reis die wordt geactiveerd wanneer Product ABC123 weer in voorraad is. Het moet een e-mail (*Productvervanging voor Luma-e-mail*) om gebruikers die het product hebben bevoordeeld terwijl het uit voorraad was, op de hoogte te stellen. De e-mail heeft een vraag-aan-actie om te beginnen winkelen.

   * In de reis, controleer of het herbevolkte punt in de verlanglijst van de klant alvorens e-mail te verzenden is.
   * Contextuele informatie toewijzen vanuit de *LumaProductRestock* gebeurtenis om de e-mail aan te passen

2. Als u een gebeurtenis voor een wensenlijst voor uzelf wilt genereren, voert u de opdracht *Studenten aan boord* Reis. Gebruik beide *LLWH06* als SKU of een andere SKU die op [Luma-website](https://publish1034.adobedemo.com/content/luma/us/en.html).

3. Als de reis eenmaal is voltooid, zet deze in de testmodus en zet deze de reis op om naar uzelf te sturen. Ben zeker om het zelfde SKU in de testgebeurtenis te gebruiken zoals u toen het teweegbrengen van de gebeurtenis van de wensenlijst in de reis van de &quot;Student Onboarding - de Gebeurtenis van de Schijflijst&quot;gebruikte

SUCCESCRITERIA

U ontvangt het product via e-mail in voorraad met het product dat u hebt opgegeven in de gebeurtenis wish list en test restock.

>[!INFO]
>
>[Uw werk controleren](/help/challenges/check-your-work/create-journeys.md) om te zien hoe de reizen eruit moeten zien.
