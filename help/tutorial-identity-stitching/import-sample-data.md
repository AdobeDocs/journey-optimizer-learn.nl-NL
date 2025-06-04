---
title: Voorbeeldgegevens van CRM importeren in AEP-profielgegevensset
description: Importeer voorbeeldrecords (bijvoorbeeld met CRMID, e-mail, inkomsten, postcode) om te controleren of AEP deze profielen correct kan koppelen aan anonieme webbezoekers op basis van gedeelde id's, zoals ECID.
feature: Profiles
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-19T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-18089
exl-id: 33c8c386-f417-45a8-83cf-7312d415b47a
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '267'
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

| crmId | firstName | lastName | email | loyaltyStatus | zipCode | jaarinkomen |
|--------|-----------|----------|-------------------------|---------------|---------|--------------|
| FIN001 | Alice | Wong | alice.wong@example.com | Goud | 92128 | 120000 |
| FIN002 | Bob | Smith | bob.smith@example.com | Zilver | 92126 | 85000 |
| FIN003 | Charlie | Kim | charlie.kim@example.com | Platina | 60614 | 175000 |
| FIN004 | Diana | Lee | diana.lee@example.com | Goud | 30303 | 98000 |
| FIN005 | Ethan | Bruin | ethan.brown@example.com | Brons | 75201 | 60000 |

## Het CSV-bestand opnemen

* Creeer een dataset genoemd **_FinWiseCustomerDataSetWithAnnualIncome_** die op **_wordt gebaseerd FinWiseProfileSchema_** in de vroegere stap wordt gecreeerd

* Ga naar Verbindingen -> Bronnen -> Lokaal systeem
* Selecteer **_Gegevens_** toevoegen onder de Lokale dossierupload. Zorg ervoor om _&#x200B;**FinWiseCustomerDataSetWithAnnualIncome**&#x200B;_ als doeldataset te selecteren.
  ![ ingest-csv ](assets/ingest-csv-into-dataset.png)
* Navigeer naar het volgende scherm. Upload het [ csv- dossier ](assets/finwise_profiles.csv) en verifieer de afbeeldingen
  ![ afbeeldingen ](assets/mappings.png)

* Klik op Voltooien om het gegevensinvoerproces te starten

## Profiel verifiëren

* Ga naar Klant ->Profielen en zoek naar FinWise CRM-id gelijk aan FIN001 of een andere geldige waarde
  ![ verifieer-profiel ](assets/verify-profiles.png)
