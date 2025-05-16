---
title: Voorbeeldgegevens van CRM importeren in AEP-profielgegevensset
description: Importeer voorbeeldrecords (bijvoorbeeld met CRMID, e-mail, inkomsten, postcode) om te controleren of AEP deze profielen correct kan koppelen aan anonieme webbezoekers op basis van gedeelde id's, zoals ECID.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
jira: KT-18089
source-git-commit: 502cdc41b666959141ff4dfc63608cc463009811
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 3%

---

# Voorbeeldgegevens van CRM importeren in AEP-profielgegevensset

Als u wilt beginnen met identiteitstitching, importeert u voorbeeld-CRM-profielgegevens in een gegevensset die is gekoppeld aan een profielschema in Adobe Experience Platform

## Een aangepaste naamruimte maken

* Ga naar Klant -> Identiteiten -> Naamruimte maken
* Selecteer Individuele apparaat-id en geef de weergavenaam en het identiteitssymbool op, zoals in de onderstaande schermafbeelding wordt weergegeven.
  ![ douane-namespace ](assets/custom-namespace.png)

## Een schema met profielinstellingen maken

Creeer een individueel profielschema genoemd **_FinWiseProfileSchema_**. Neem velden op, zoals annualIncome, email,firstName,lastName en loyaltyStatus.
Voeg een identiteitsgebied **_toe midden_** onder het voorwerp SystemIdentifier. Het tussentijdse veld markeren als identiteit en primair


![ profiel-schema ](assets/finwise-profile-schema.png)

## Voorbeeldgegevens voorbereiden

| crmId | firstName | lastName | email | loyaltyStatus | jaarinkomen |
|--------|-----------|----------|---------------------------|---------------|--------------|
| FIN001 | Alice | Wong | alice.wong@example.com | Goud | 336104 |
| FIN002 | Brian | Smith | brian.smith@example.com | Zilver | 191065 |
| FIN003 | Cathy | Johnson | cathy.johnson@example.com | Brons | 117015 |
| FIN004 | David | Lee | david.lee@example.com | Brons | 61869 |
| FIN005 | Eva | Martinez | eva.martinez@example.com | Zilver | 191371 |
| FIN006 | Frank | Bruin | frank.brown@example.com | Zilver | 196132 |
| FIN007 | Grace | Kim | grace.kim@example.com | Goud | 309851 |
| FIN008 | Henry | Davis | henry.davis@example.com | Goud | 318378 |
| FIN009 | Isla | Clark | isla.clark@example.com | Zilver | 181776 |
| FIN010 | Jack | Lopez | jack.lopez@example.com | Zilver | 186643 |

## Het CSV-bestand opnemen

* Creeer een dataset genoemd **_FinWiseCustomerDataSetWithAnnualIncome_** die op **_wordt gebaseerd FinWiseProfileSchema_** in de vroegere stap wordt gecreeerd

* Ga naar Verbindingen -> Bronnen -> Lokaal systeem
* Selecteer **_Gegevens_** toevoegen onder de Lokale dossierupload. Zorg ervoor om _&#x200B;**FinWiseCustomerDataSetWithAnnualIncome**&#x200B;_ als doeldataset te selecteren.
  ![ ingest-csv ](assets/ingest-csv-into-dataset.png)
* Navigeer naar het volgende scherm. Upload het [ csv- dossier ](assets/sample_crm_data.csv) en verifieer de afbeeldingen
  ![ afbeeldingen ](assets/mappings.png)

* Klik op Voltooien om het gegevensinvoerproces te starten

## Profiel verifiëren

* Ga naar Klant ->Profielen en zoek naar FinWise CRM-id gelijk aan FIN001 of een andere geldige waarde
  ![ verifieer-profiel ](assets/verify-profiles.png)
