---
title: Personalization met JSON-inhoud leveren in Adobe Journey Optimizer
description: Gebruik het JSON-inhoudssoort in Adobe Journey Optimizer (AJO) om flexibele, gegevensgestuurde personalisatieervaringen op te bouwen.
feature: Decisioning
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2025-06-18T00:00:00Z
jira: KT-18387
recommendations: noDisplay, noCatalog
source-git-commit: 9f5b52063605832a9b00c05fb1a93bf60ec7686f
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Personalization met JSON-inhoud leveren in Adobe Journey Optimizer

Deze sectie wordt verstrekt als extra middel voor gevorderde gebruikers die grotere controle over willen hoe de aanbiedingen op het vooreind worden teruggegeven.

Met het JSON-inhoudstype in een CBE (Code-Based Experience) kunt u gestructureerde aanbiedingsgegevens retourneren en rendering dynamisch verwerken met behulp van JavaScript. Het JSON-inhoudssoort is vooral handig voor scenario&#39;s waarvoor aangepaste indelingen, voorwaardelijke logica of integratie met contextuele gegevens nodig zijn, zoals weer, locatie of apparaattype.

Hoewel deze aanpak niet vereist is voor de levering van basisaanbiedingen, biedt deze flexibiliteit voor ontwikkelaars die persoonlijke, gegevensgestuurde ervaringen opbouwen die verder gaan dan de mogelijkheden van standaard HTML-rendering.

## Maak een CBE (Code-Based Experience) met het JSON-inhoudstype.

Maak eerst een nieuwe CBE (Code-Based Experience) in Adobe Journey Optimizer en stel de Inhoudsindeling in op JSON. Het inhoudstype vertelt AJO om gestructureerde aanbiedingsgegevens (zoals offerText, beelden, of meta-gegevens) als voorwerp JSON eerder dan teruggegeven HTML terug te keren. Definieer het platform (bijvoorbeeld Web), de doel-URL waar de aanbieding verschijnt en de locatie op de pagina (zoals een container-id zoals offerContainer). Met deze configuratie kan uw webtoepassing aanbiedingsgegevens ontvangen en deze dynamisch renderen met JavaScript.

![ json-content-type ](assets/cbe-json-content.png)

## De CBE koppelen aan een campagne met een beslissingsbeleid

Zodra de code-Gebaseerde Ervaring (CBE) met JSON inhoudstype wordt gecreeerd, is het verbonden met een campagne door een Beleid van het Besluit. In het beslissingsbeleid wordt de logica voor het aanbieden van de subsidiabiliteit, rangschikking en levering gedefinieerd op basis van profiel of contextuele gegevens.

Wanneer u het beslissingsbeleid invoegt in de Personalization Editor (bijvoorbeeld voor berichten in de app of e-mail), is het belangrijk dat de uitvoer een geldige JSON-structuur behoudt.

Wanneer u een Beleid van het Besluit in de Redacteur van Personalization (PE) binnen een campagne opneemt, produceert Adobe Journey Optimizer automatisch een lijn Handlebars die op het geselecteerde beleid wordt gebaseerd. Bijvoorbeeld:
![ gebrek-code ](assets/handlebar-code-default.png)
Deze lijn herhaalt door alle besluitvormingspunten die door het beleid zijn teruggekeerd en injecteert het aanbiedingstekstgebied van elke aanbieding. Deze standaardstructuur werkt goed voor HTML-inhoudssoorten, maar wanneer u met JSON-inhoud werkt, kan het zijn dat u een herstructurering moet uitvoeren om een geldige JSON-array of -object te maken, vooral als het resultaat programmatisch wordt geparseerd.

![ herstructureerde-code ](assets/restructured-code.png)

Deze sjabloon Handlebars is ontworpen om een serie van JSON van aanbiedingsvoorwerpen uit te voeren, waar elk voorwerp één één aanbiedingstekstgebied bevat. Het doorloopt de besluitvormingspunten door het gespecificeerde Beleid van het Besluit zijn teruggekeerd en verpakt elke aanbiedingText in een JSON objecten formaat.

## Parse JSON-respons

De reactie van AJO bevat gepersonaliseerde beslissingsitems in JSON-indeling onder de `propositions[].items[].data.content[]` -structuur. Elk inhoudsitem bevat velden zoals offerText.

```javascript
(response.propositions || []).forEach(p => {
  (p.items || []).forEach(item => {
    const contents = item.data?.content || [];
    contents.forEach(contentItem => {
      const html = contentItem.offerText || "";
      const wrapper = document.createElement("div");
      wrapper.className = "offer";
      wrapper.innerHTML = html;
      document.getElementById("offerContainer").appendChild(wrapper);
    });
  });
});
```

### Voorbeeldelementen

Download het voorbeeld-HTML-bestand en het JavaScript-bestand, die aantonen hoe u op JSON gebaseerde aanbiedingen kunt gebruiken en deze dynamisch op uw webpagina kunt weergeven, zodat u aan de slag kunt.

[ code van JavaScript ](assets/weather-related-offers-script-multiple-json.js)
[ HTML- Dossier ](assets/multiple-json.html)