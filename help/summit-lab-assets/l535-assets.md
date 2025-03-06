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
source-git-commit: c1a77892652df0a91a6add1ad0dc5a4bd0770d8b
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Top Lab L535 - Cheat Sheet

Deze pagina bevat tekst en koppelingen die worden gebruikt in het Lab van de L535-top. Hiermee kunt u de inhoud naar Journey Optimizer-berichten kopiëren en plakken.

## Koppelingen

* [ Adobe Journey Optimizer ](https://experience.adobe.com/#/@techmarketingdemos/sname:ajo-summit-lab/journey-optimizer/journeys)
* [ SecurFinancial Website ](https://dsn.adobe.com/web/hausmann-FTTN?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsIm5hbWUiOiJBbm9ueW1vdXMiLCJpc1N1cGVyVXNlciI6ZmFsc2UsImlzc3VlciI6ImhhdXNtYW5uIiwicHJvamVjdHMiOnsiaGF1c21hbm4tRlRUTiI6InZpZXcifSwiaWF0IjoxNzQwNzU2NTYxLCJleHAiOjE3NDMzNDg1NjF9.ryOTsqDH9B33436RlIo4AHFxx8aGjNEMqv9FAxLZb9U)
* [ Download app ](https://demo-system-next.s3.amazonaws.com/dxdemo/summit/index.html)

## Kopiëren en plakken voor oefeningen

### Oefening 2.3 - Het e-mailbericht samenstellen

#### Vragen

```
Generate a welcome email for new SecurFinancial customers who just opened a new savings account. 
Add a call to action to install the SecurFinancial mobile app.
```

### Oefening 3.1 - Dynamische inhoud toepassen op het SMS-bericht

#### Code

```
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

### Oefening 4.2 - De behandelingen configureren

#### Titel

```
Welcome to SecurFinancial
```

#### Platte tekst

```
Did you know you can find an ATM near in the SecurFinancial app? Try it now!
```

#### URL

```
dxdemo://atm
```

### Oefening 6 - Inhoudskaarten

#### Titel

```
Welcome to SecurFinancial!
```

#### Lichaam

```
Thank you for downloading the app. You can find ATMs, track your spending and more. All within the app.
```

#### Media-URL

```
https://demo-systemnext.s3.amazonaws.com/assets/securfinancial/homeloan.jpg
```

#### Knoptitel

```
Find ATMs
```

#### Doel-URL

```
dxdemo://atm
```

## Afbeeldingen

![ SecureFinancial embleem ](/help/summit-lab-assets/assets/SecureFinancial-logo.png)


![ Mobiele Telefoon ](/help/summit-lab-assets/assets/online-banking-app-01.png)


