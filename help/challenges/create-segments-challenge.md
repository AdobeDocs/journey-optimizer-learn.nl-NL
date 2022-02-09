---
title: Uitdaging 1 - Segmenten maken
description: Pas toe wat u hebt geleerd over het maken van segmenten en test uw vaardigheden.
kt: 8417
feature: Segments
role: User
level: Beginner
source-git-commit: 676f0b268f7f67d179bfa944b72cb68191640c74
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Uitdaging 1 - Segmenten maken

## Het artikel

Luma, een fictioneel atletisch kledingbedrijf, wil zijn nieuwste kleding- en tandwielcollectie promoten en de verkoop voor bestaande klanten stimuleren. Om de nieuwe inzamelingscampagne te steunen, vraagt het marketing team van Luma u om tot stand te brengen [segmenten](/help/set-up-resources/create-segments.md) die nodig zijn om de reis voor de campagne te maken.

## Uw uitdaging

Maak de volgende segmenten in Journey Optimizer.

### Segment #1 - Actieve klanten

Creeer een publiek aan doel met de nieuwe mededeling van de zomerinzameling:

* Geef dit segment een naam *uw naam - Actieve Klanten*
* Het publiek mag alleen actieve Luminantieklanten bevatten. Actieve klanten worden gedefinieerd als klanten met een laag in het loyaliteitsprogramma van Luma (zilver, goud, platina of diamant)

**SUCCESCRITERIA**

1. In de segmentbouwer, kunt u het geschatte aantal gekwalificeerde profielen zien. Als u in de trainingssandbox werkt, moet dit getal gelijk zijn aan of groter zijn dan 0.
2. Er is een in aanmerking komend profiel toegevoegd aan het segment:
   * U kunt controleren of een profiel aan het segment is toegevoegd door naar een van de profielen te navigeren die op het tabblad Details worden vermeld.
   * Voor de profielpagina, controleer de attributen om te bevestigen dat zij kwalificeren en dan het segmentlidmaatschap controleren.

+++**UW WERK CONTROLEREN**
De reeks selecteren (CDM-profiel > Loyalty> Tier)

Zo ziet uw segment eruit:

![Segment #1 - Actieve klanten](/help/challenges/assets/C1-S1.png)

Controleer de code in de rechterbenedenhoek van het scherm Segment bewerken onder Gebeurtenissen. De code moet er als volgt uitzien:

loyalty.tier.equals(&quot;diamond&quot;, false) of loyalty.tier.equals(&quot;goud&quot;, false) of loyalty.tier.equals(&quot;platinum&quot;, false) of loyalty.tier.equals(&quot;zilver&quot;, false)

+++

## Segment nr. 2 - Afgedankte items op de Wishlist

Om potentiële geïnteresseerde klanten te richten wanneer de producten worden herbevolkt, creeer een publiek dat uit klanten bestaat

* die een item aan hun wenslijst hebben toegevoegd (gebeurtenistype Opslaan voor later)
* die in de laatste drie maanden niet in voorraad was,
* en hebben het object sindsdien niet gekocht.

Geef dit segment een naam: *uw naam - Verouderd*

**SUCCESCRITERIA**

TBD