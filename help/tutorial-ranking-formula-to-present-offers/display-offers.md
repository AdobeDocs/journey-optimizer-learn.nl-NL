---
title: Creeer een Web-pagina om de Oplossing te testen
description: Web-pagina om de gepersonaliseerde aanbiedingen te testen die gebruikend besluit worden geleverd.
role: User
level: Beginner
doc-type: Tutorial
feature: Decisioning
last-substantial-update: 2025-05-31T00:00:00Z
jira: KT-18188
recommendations: noDisplay, noCatalog
exl-id: 6b1eec78-153c-4ea5-acfe-2dcc6f1e6078
source-git-commit: 82d82b3aac2bf91e259b01fd8c6b4d6065f9640a
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Creeer een Web-pagina om de Oplossing te testen

Deze voorbeeldtoepassing simuleert een real-world login stroom waar de gebruikersgeloofsbrieven op de server worden bevestigd alvorens identiteitskaart van CRM naar Adobe Experience Platform (AEP) wordt verzonden. Een lokale server Node.js wordt gebruikt om de Web-pagina&#39;s veilig te dienen, basisauthentificatielogica te behandelen, en browser beperkingen (zoals geblokkeerde lokale dossiertoegang of ontbrekende kopballen van CORS) te vermijden die de functionaliteit van de Lancering van Adobe of van het Web SDK konden interfereren. Deze opstelling zorgt ervoor dat de ervaring aan een echte productiemilieu dichter is.

Aangepaste aanbiedingen worden alleen weergegeven nadat de gebruiker zich heeft aangemeld. Op dat moment wordt het aanpassen van de identiteit tussen de CRM-id van de gebruiker en de ECID (Experience Cloud-id) voltooid. Deze identiteitsbevestiging zorgt ervoor dat Adobe Journey Optimizer (AJO) het profiel en de beoogde retouraanbiedingen nauwkeurig kan herkennen.

Nadat de aanmelding is voltooid, wordt een verzoek tot personalisatie naar AJO verzonden om de beschikbare aanbiedingen voor de gebruiker op te halen. Deze aanbiedingen worden geretourneerd als HTML-fragmenten, die elk zijn ingesloten met een kenmerk data-tags — zoals data-tags=&quot;ajo offer-vacation-based-cd zip-92128 inkomen-high&quot; — dat de naam van de aanbieding en segmentatiedetails zoals ZIP-code en het inkomensniveau bevat.

JavaScript parseert deze HTML-blokken en plaatst ze in een carrousel-item container. De items worden horizontaal in een carrouseltrack geplaatst, zodat u snel kunt navigeren. Met de knoppen Vorige en Volgende (◀ en ▶ ) kunnen gebruikers de gepersonaliseerde aanbiedingen een voor een doorlopen.

Deze opstelling verstrekt een ontvankelijke en op maat gemaakte ervaring, die ervoor zorgt dat elke gebruiker aanbiedingen relevant voor hun financieel profiel ziet — slechts nadat hun identiteit veilig over platforms is vastgemaakt.

## Deze oplossing testen

* Creeer een omslag genoemd rangschikkend-formule binnen uw bestaand project Node.js.

* Pak de [ verstrekte dossiers in deze rangschikking-formule omslag uit.](assets/ranking-formula.zip)

* Voer de app uit door naar de map te navigeren en de server te starten:
   * `cd ranking-formula`

   * `node server.js`


* Open uw browser en ga naar http://localhost:3000/formula.html.

* Aanmelden met ijs/pass123

Omdat Alice in de ZIP-code 92128 verblijft, worden aanbiedingen die op die locatie zijn afgestemd, weergegeven.
