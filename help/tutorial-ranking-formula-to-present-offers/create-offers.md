---
title: Locatiegebaseerde voorstellen maken met ZIP-codering als doel
description: Een aanbiedingsitem in de besluitvorming vertegenwoordigt één stuk gepersonaliseerde inhoud, zoals een bericht, afbeelding, promotie of aanbeveling, dat aan een gebruiker kan worden geleverd op basis van gedefinieerde regels en voorwaarden.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-05-30T00:00:00Z
jira: KT-18188
source-git-commit: 58d2964644bc199b9db212040676d87d54f767b9
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Locatiegebaseerde voorstellen maken met ZIP-codering als doel

Voordat u de aanbiedingen maakte, is het schema Item van voorstel uitgebreid met een nieuw veld: zipcode. Dit douanegebied laat elke aanbieding toe om uitdrukkelijk met zijn doelZIP code worden geëtiketteerd, die voor op plaats-gebaseerde het filtreren en rangschikken tijdens besluit toestaat.

Met bijgewerkt schema, werden twee gepersonaliseerde aanbiedingen gecreeerd:

* Aanbieding 1: &quot;Flexible Investment Plans for Mira Mesa (92126)&quot;
Dit aanbod, dat in 92126 is toegesneden op jonge professionals en op technologie gerichte ingezetenen, bevordert flexibele investeringsopties zoals ETF&#39;s en onderlinge fondsen die gericht zijn op langetermijngroei. Het veld Postcode is ingesteld op 92126.

* Aanbieding 2: &quot;CD&#39;s met hoog rendement voor Rancho Bernardo (92128)&quot;
Deze aanbieding is gericht op financieel stabiele en voor pensionering geschikte personen in 92128 en bevat hoogrenderende depositocertificaten (cd&#39;s) met een gegarandeerd rendement. Het veld Postcode is ingesteld op 92128.

Deze aanbiedingen worden nu verrijkt met locatiemetagegevens, waardoor ze in latere stappen in aanmerking komen voor dynamische selectie en rangschikking op basis van ZIP-codes van gebruikersprofielen.

De volgende schermafbeelding toont de aangepaste kenmerken die zijn toegevoegd aan het schema van het aanbiedingsitem.

![ aanbiedingen-meta-gegevens ](assets/offers-meta-data.png)


## Voorstel voor 92126

De aanbiedingstekst voor aanbiedingen in ZIP-code 92126

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #f9f9f9; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">   <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">     Boost Your Financial Game with Smart Investment Options   </h2>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     In Mira Mesa (92126), ambition meets opportunity. Whether you're building wealth or just getting started, our     <strong>diversified investment plans</strong> — including <strong>tech-focused ETFs</strong> and     <strong>flexible mutual funds</strong> — are designed to grow with your goals.   </p>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Enjoy expert guidance, low fees, and strategies built for busy professionals who want more from their money — without the hassle.   </p>   <a href="#start-investing" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">     Start Investing Smarter   </a> </div>
```


## Voorstel voor 92128

De aanbiedingstekst voor aanbiedingen in ZIP-code 92128

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #fdfdfd; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">   <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">     Grow Your Savings with Confidence – Exclusive CD Rates for 92128   </h2>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Live in Rancho Bernardo? Take advantage of your financial momentum with our <strong>high-yield Certificates of Deposit</strong>, offering up to <strong>5.25% APY</strong>.     Designed for peace of mind and smart growth, our flexible CD options let you lock in guaranteed returns while enjoying the stability you deserve.   </p>   <p style="color: #333; font-size: 1rem; line-height: 1.6;">     Whether you're planning retirement or simply securing your future, this offer is tailored for residents like you.   </p>   <a href="#explore-cd-options" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">     Explore CD Options   </a> </div>
```

## Generieke aanbieding (Fallback-aanbieding)

De aanbiedingstekst voor Algemene aanbieding, zonder postcode die aan de aanbieding is gekoppeld

```html
<div style="max-width: 600px; margin: 2rem auto; padding: 1.5rem; border: 1px solid #ddd; border-radius: 12px; font-family: Arial, sans-serif; background-color: #ffffff; box-shadow: 0 4px 12px rgba(0,0,0,0.05);">
  <h2 style="color: #1a237e; font-size: 1.5rem; margin-bottom: 0.5rem;">
    Invest Smarter: Build Wealth with Flexible Financial Plans
  </h2>
  <p style="color: #333; font-size: 1rem; line-height: 1.6;">
    Looking to take control of your financial future? Our flexible investment solutions are designed to meet a wide range of goals — from growing savings to planning for retirement.
    Choose from diversified mutual funds, ETFs, and professionally managed portfolios, all with expert guidance and minimal hassle.
  </p>
  <p style="color: #333; font-size: 1rem; line-height: 1.6;">
    Whether just starting out or optimizing an existing strategy, this offer provides the tools to invest with confidence — no matter where you live.
  </p>
  <a href="#explore-investment-plans" style="display: inline-block; margin-top: 1rem; background-color: #1a73e8; color: white; padding: 0.75rem 1.25rem; border-radius: 8px; text-decoration: none; font-weight: bold;">
    Explore Investment Plans
  </a>
</div>
```

Groep deze aanbiedingen in een inzameling genoemd **_GenericOffers_**

De aanbiedingen zijn beschikbaar voor alle bezoekers—wat betekent dat er geen strikte toelatingsbeperkingen zijn—en de rangschikkingsformule wordt dan van essentieel belang om te bepalen welke aanbieding op profielcontext zou moeten worden getoond.
Aangezien de toelatingsregels de aanbiedingen niet filtreren, worden alle drie behandeld als kandidaten.
De selectiestrategie haalt alle drie op.
De rangschikkende formule scores hen die op profielattributen (zoals zipcode en annualIncome) worden gebaseerd om beste te kiezen.



