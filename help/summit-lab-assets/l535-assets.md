---
title: L535 Cheat Sheet
description: Deze pagina bevat tekst en koppelingen die worden gebruikt in het Lab van de L535-top.
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: 1c3f4341-1293-463d-bee0-57440fcff23a
source-git-commit: 51ab40981a42b0df56d3994f1155eb4ae7575b17
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# Top Lab L535 - Cheat Sheet

Deze pagina bevat tekst en koppelingen die worden gebruikt in het Lab van de L535-top. Hiermee kunt u de inhoud naar Journey Optimizer-berichten kopiëren en plakken.

## Koppelingen

* [ Adobe Journey Optimizer ](https://experience.adobe.com/#/@techmarketingdemos/sname:ajo-summit-lab/journey-optimizer/journeys)
* [ SecurFinancial Website ](https://dsn.adobe.com/web/hausmann-FTTN?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsIm5hbWUiOiJBbm9ueW1vdXMiLCJpc1N1cGVyVXNlciI6ZmFsc2UsImlzc3VlciI6ImhhdXNtYW5uIiwicHJvamVjdHMiOnsiaGF1c21hbm4tRlRUTiI6InZpZXcifSwiaWF0IjoxNzQwNzU2NTYxLCJleHAiOjE3NDMzNDg1NjF9.ryOTsqDH9B33436RlIo4AHFxx8aGjNEMqv9FAxLZb9U)
* [ Download app ](https://demo-system-next.s3.amazonaws.com/dxdemo/summit/index.html)

## Uitoefening

### Oefening 2.3

**Stap 12** E-mailberichtherinnering:

Een welkomstbericht genereren voor nieuwe SecurFinancial
klanten die zojuist een nieuwe spaarrekening hebben geopend. Voeg een
oproep tot actie om de mobiele app SecurFinancial te installeren.

### Oefening 3.1

**Stap 7**

```javascript
{%#if select _Push_details1 from profile.pushNotificationDetails where
_Push_details1.token.isNotNull()%}
Welcome to your new SecurFinancial checking account! Discover the
SecurFinancial mobile app, designed for effortless banking. Manage accounts,
transfer funds, and monitor transactions securely, anytime, anywhere. Open the
app
{%else%}
Welcome to your new SecurFinancial checking account! Discover the
SecurFinancial mobile app, designed for effortless banking. Manage accounts,
transfer funds, and monitor transactions securely, anytime, anywhere. Click here
to install the app: https://demo-systemnext.
s3.amazonaws.com/dxdemo/summit/index.html
{%/if%} 
```


![ SecureFinancial embleem ](/help/summit-lab-assets/assets/SecureFinancial-logo.png)

![ Mobiele Telefoon ](/help/summit-lab-assets/assets/online-banking-app-01.png)


