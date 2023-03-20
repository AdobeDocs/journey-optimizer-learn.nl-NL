---
title: L731 Kauwblad
description: Deze pagina bevat tekst en koppelingen die worden gebruikt in het Lab van de L731-top.
feature: In App, SMS, Push, Email
doc-type: article
role: User
level: Beginner
recommendations: noDisplay, noCatalog
hide: true
hidefromtoc: true
exl-id: ffc5e8c8-8729-4e7e-aa51-d74f91b0cf29
source-git-commit: ea4ba49056ad3e575c0953ad963966bcecf54c9f
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---

# Top Lab L731 - Cheat Sheet

Deze pagina bevat tekst en koppelingen die worden gebruikt in het Lab van de L731-top. Hiermee kunt u de inhoud naar Journey Optimizer-berichten kopiëren en plakken.

## Oefening 1.1 - De app downloaden en installeren

Scan de QR-code om de app te downloaden

>[!BEGINTABS]

>[!TAB iOS]

![QR-code voor iOS](/help/assets/lab731-ios-qr-code.png)

U wordt gevraagd Testflight te installeren (stappen 1 tot en met 4). Nadat u Testflight hebt geïnstalleerd, voert u de stappen 5 tot en met 8 uit om de Las van Vegas te installeren:

<table>
<tr>
</tr>
<tr>
<td>
 <div>
      <p>
      <b>Stap 1 </b>
      <p>
      <a href="Step 1:">
        <img alt="testvlucht 1" src="../assets/l731-ios-install/ios-install-1.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Stap 2 </b>
      <p>
      <a href="Step 1:">
        <img alt="testvlucht 1" src="../assets/l731-ios-install/ios-install-2.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Stap 3 </b>
      <p>
      <a href="Step 1:">
        <img alt="testvlucht 1" src="../assets/l731-ios-install/ios-install-3.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Stap 4 </b>
      <p>
      <a href="Step 4">
        <img alt="testvlucht 1" src="../assets/l731-ios-install/ios-install-4.PNG"/>
      </a>
      </div>
  </td>
  </tr>
  <tr>
<td>
 <div>
      <p>
      <b>Stap 5 </b>
      <p>
      <a href="Step 1:">
        <img alt="testvlucht 1" src="../assets/l731-ios-install/ios-install-5.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Stap 6 </b>
      <p>
      <a href="Step 1:">
        <img alt="testvlucht 1" src="../assets/l731-ios-install/ios-install-6.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Stap 7 </b>
      <p>
      <a href="Step 1:">
        <img alt="testvlucht 1" src="../assets/l731-ios-install/ios-install-7.PNG"/>
      </a>
      </div>
  </td>
  <td>
 <div>
      <p>
      <b>Stap 8 </b>
      <p>
      <a href="Step 4">
        <img alt="testvlucht 1" src="../assets/l731-ios-install/ios-install-8.PNG"/>
      </a>
      </div>
  </td>
  </tr>
</table>
&gt;[!TAB Android™]

![QR-code voor Android](/help/assets/lab731-android-qr-code.png)

Gebruik de volgende koppeling als u de Android-simulator gebruikt: [https://ajolab.s3.amazonaws.com/ajolabapp-release.apk](https://ajolab.s3.amazonaws.com/ajolabapp-release.apk)

Aangezien de app niet bij de Google Play Store is geregistreerd, ontvangt u een waarschuwingsbericht:

![Android-waarschuwingsscherm](/help/assets/lab731-install-android.png)

Klikken **Toch installeren**

>[!ENDTABS]

## Oefening 1.3: Aanmelden bij Adobe Journey Optimizer

[Klik hier om u aan te melden bij Journey Optimizer](https://experience.adobe.com/#/@techmarketingdemos/sname:summit-2023-ajo-lab/journey-optimizer/home)

**Aanmeldingsgegevens:**

* **Gebruikersnaam:** `L731+<your seat number>@summitlab.us` (voorbeeld: L731+001@summitlab.us)
* **Wachtwoord:** Adobe 2023!


## Oefening 2.1 Een campagne in de app maken

| Veld | Tekst | Koppelingen |
|----|----|----|
| Campagnenaam | `<your seat number> March Vegas Campaign` |  |
| Matcher | oplichten |  |
| Media-URL, optie |  | https://mcfadyen.com/wp-content/uploads/2023/01/Adobe-Summit-2023-Banner.png |
| Titel | Het gebeurt en het is live! |  |
| Lichaam | Adobe Summit keert terug naar Las Vegas March 21-23, 2023. Bereid u voor op inspirerende luidsprekers, sessies die de vaardigheden uitbreiden en nieuwe verbindingen. |  |
| Knop | Boekhotel nu en bespaar 10% | lab://booking?suite=presidential&amp;discount=10 |
| Knop: Interactieve gebeurtenis | CTA in de app |  |
| Basis-URL |  | iOS: lab:// <br>Android™: https://lab |


## Les 3 Een OmniChannel-reis maken

**Reislabel:**
<your seat number> - Welkomstreis

>[!BEGINTABS]

>[!TAB Push-bericht]

**Label:**
Welkomstbericht

**Titel:**\
Welkom in Vegas!

**Lichaam:**\
De regel overslaan en inchecken met de mobiele app

**Deëplink:** lab://checkin

**Media:**

https://experienceleague.adobe.com/docs/journey-optimizer-learn/assets/vegas_online_check_in.jpg?lang=en


Dit is de afbeelding die we gebruiken voor de pushmelding:

![Online inchecken](/help/assets/vegas_online_check_in.jpg)

>[!TAB SMS-bericht]

**Label:**
Welkomstbericht

**Bericht:**
Welkom in Vegas. De regel overslaan en inchecken met de mobiele app: lab://checkin

>[!TAB E-mailbericht]

**Label:**
Bevestigingsbericht

**Onderwerpregel:**
{{profile.person.name.firstName}}, je bent aangemeld. Bekijk nu onze voorstellen voor je verblijf!

>[!ENDTABS]
