---
title: Een voorstel maken
description: Een aanbiedingsitem in de besluitvorming vertegenwoordigt één stuk gepersonaliseerde inhoud, zoals een bericht, afbeelding, promotie of aanbeveling, dat aan een gebruiker kan worden geleverd op basis van gedefinieerde regels en voorwaarden.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-05T00:00:00Z
recommendations: noDisplay, noCatalog
jira: KT-17728
exl-id: d705992a-0d47-4bb9-b3d8-b925974e64cb
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# Een aanbieding maken

Een aangeboden object in AJO vertegenwoordigt één stuk gepersonaliseerde inhoud. De inhoud kan een bevordering, een bericht, of een aanbeveling zijn die aan een gebruiker, op besluitvormingslogica wordt geleverd.

Wanneer u een aanbiedingspunt in AJO creeert, moet het op het Schema van de Beslissing van a  worden gebaseerd. Dit schema definieert de structuur en velden die beschikbaar zijn in de aanbieding, zoals titel, beschrijving, imageURL, aanbiedingText enzovoort.

Dit schema:

* Hiermee wordt het inhoudsmodel gestandaardiseerd voor alle aanbiedingen in een verzameling.

* Staat verenigbare verpersoonlijkingsgebieden over aanbiedingspunten toe.

* Hiermee worden selectiestrategieën afgestemd op gestructureerde inhoud

## Het schema wijzigen

1. Meld u aan bij Journey Optimizer.
1. Klik **[!UICONTROL Beslissing]** > **[!UICONTROL Catalogi]** > **[!UICONTROL geef schema]** uit.
1. Een element van het type `string` genaamd `offerItem` toevoegen, zoals hieronder wordt weergegeven

   ![ besluit-schema ](assets/offer-schema.png)

## Een aangeboden object maken

1. Klik **[!UICONTROL Beslissing]** > **[!UICONTROL Catalogi]** > **[!UICONTROL creeer punt]**.

1. Maak drie aanbiedingen: `Love Stocks`, `Love Bonds` en `Love CD` .

   Kopieer en plak voor elke aanbieding de tekst van de desbetreffende aanbieding aan het einde van dit artikel in het betreffende aanbiedingsobject.

1. Geef de aanbiedingen een label met de tag die u in de vorige stap hebt gemaakt.
1. Voeg een passend publiek toe aan elke aanbieding.
   ![ aanbieding-geschiktheid ](assets/offer-eligibility.png)
1. Goedkeuren van de voorstellen.

Voltooide aanbieding met gedefinieerde standaard- en aangepaste kenmerken:

![ aanbieding van de liefdesaandelen ](assets/love-bonds.png)

**de Stocks van de Liefde biedenText**

```html
<div style="font-family: Arial, sans-serif; background-color: #f9f9f9; border: 1px solid #ddd; padding: 1.5rem; border-radius: 8px; max-width: 600px; margin: auto;">   <h3 style="color: #1a73e8; margin-top: 0;">📈 Open a Stock Trading Account & Get $100 in Bonus Stock</h3>   <p style="font-size: 1rem; color: #333;">     Ready to start building your portfolio? Open a new stock trading account with us and receive a      <strong>$100 bonus in stock</strong> — on us.   </p>   <ul style="padding-left: 1.25rem; color: #444;">     <li>🧾 No account minimums — start investing with as little as $1</li>     <li>📉 $0 commissions on online stock trades</li>     <li>📊 Access to powerful trading tools and real-time analytics</li>     <li>🎓 Free educational resources to help you invest confidently</li>   </ul>   <p style="color: #333;">     It's never been easier to start trading. Join thousands of investors who trust us to help them grow their wealth.   </p>   <a href="https://yourbrokerage.com/open-account"      style="display: inline-block; margin-top: 1rem; padding: 0.75rem 1.5rem; background-color: #1a73e8; color: white; text-decoration: none; border-radius: 5px; font-weight: bold;">      🚀 Open Your Account Today   </a> </div>
```

**de Obligaties van de Liefde biedenText**

```html
<div style="font-family: Arial, sans-serif; background-color: #f9f9f9; border: 1px solid #ddd; padding: 1.5rem; border-radius: 8px; max-width: 600px; margin: auto;">   <h3 style="color: #6c757d; margin-top: 0;">🏦 Invest in Stability: Explore Our Premium Bond Options</h3>   <p style="font-size: 1rem; color: #333;">     Looking for consistent income with lower risk? Our carefully selected bonds offer predictable returns and help balance your investment portfolio.   </p>   <ul style="padding-left: 1.25rem; color: #444;">     <li>📉 Lower volatility than stocks — ideal for income-focused investors</li>     <li>💵 Earn interest payments monthly, quarterly, or annually</li>     <li>🔍 Choose from government, municipal, or corporate bonds</li>     <li>🎁 Open a bond investment account today and receive a <strong>$50 interest credit</strong></li>   </ul>   <p style="color: #333;">     Whether you're preparing for retirement or just want a reliable stream of income, bonds offer a solid foundation for your financial strategy.   </p>   <a href="https://yourfirm.com/open-bond-account"      style="display: inline-block; margin-top: 1rem; padding: 0.75rem 1.5rem; background-color: #6c757d; color: white; text-decoration: none; border-radius: 5px; font-weight: bold;">      🧾 Open a Bond Account   </a> </div>
```

**van de Liefde CD offerText**

```html
<div style="font-family: Arial, sans-serif; background-color: #f9f9f9; border: 1px solid #ddd; padding: 1.5rem; border-radius: 8px; max-width: 600px; margin: auto;">   <h3 style="color: #28a745; margin-top: 0;">💰 Lock in a 5.25% APY — Open Your CD Account Today</h3>   <p style="font-size: 1rem; color: #333;">     Secure your savings with a high-yield Certificate of Deposit. For a limited time, enjoy a      <strong>guaranteed 5.25% annual percentage yield (APY)</strong> on 12-month CDs.   </p>   <ul style="padding-left: 1.25rem; color: #444;">     <li>🔒 Guaranteed returns with FDIC insurance</li>     <li>📈 Lock in today's high rates before they change</li>     <li>💼 Flexible terms from 6 to 24 months</li>     <li>🎁 Open with just $500 and get a $50 bonus</li>   </ul>   <p style="color: #333;">     Whether you're saving for a short-term goal or building a conservative income strategy, our CDs offer peace of mind and predictable growth.   </p>   <a href="https://yourbank.com/open-cd"      style="display: inline-block; margin-top: 1rem; padding: 0.75rem 1.5rem; background-color: #28a745; color: white; text-decoration: none; border-radius: 5px; font-weight: bold;">      💼 Open a CD Account   </a> </div>
```
