---
title: Foutopsporing op het web in AJO
description: Deze pagina biedt handige tips voor foutopsporing in de berichtstroom van webpushberichten, waaronder het controleren van SDK-aanvragen voor webpagina's.
feature: Push
role: User
level: Beginner
doc-type: Tutorial
last-substantial-update: 2026-04-21T00:00:00Z
jira: KT-20879
source-git-commit: 45f86aeb8fca071436785cc55225d853bb21998f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Foutopsporing op het web in AJO

Deze pagina biedt handige tips voor het opsporen van fouten in de berichtstroom van webpushberichten, zoals het controleren van SDK-aanvragen, het controleren van de ECID en het gebruikersprofiel in AEP en het controleren van gebeurtenissen zoals price.drop die correct zijn verzonden en ontvangen.

- **gebruik Adobe Experience Platform Debugger (de Uitbreiding van Chrome)**\
  Installeer de [&#x200B; Debugger van AEP uitbreiding voor Chrome &#x200B;](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob) om de activiteit van SDK van het Web gemakkelijker te inspecteren:

Met dit gereedschap kunt u:
- Webverzoeken en reacties van SDK weergeven\
- Controleer de ECID (Experience Cloud-id)\
- Configuratie en nuttige taken van gegevensstroom valideren

- **Controle als de gebruiker (ECID) wordt geïdentificeerd**\
  Gebruik Foutopsporing van AEP of de browserconsole om te bevestigen dat een ECID is gegenereerd. Deze id wordt gebruikt om de gebruiker in AEP en AJO bij te houden.

- **Gebruik het lusje van het Netwerk om verzoeken** te verifiëren\
  Open het **lusje van het Netwerk** in de ontwikkelaarshulpmiddelen van uw browser en filter voor verzoeken die door SDK van het Web worden gemaakt (zoek `/collect` of `interact`).
   - Bevestig verzoeken worden verzonden wanneer de pagina wordt geladen en wanneer handelingen worden geactiveerd
   - Controleer of de gebeurtenis `price.drop` is opgenomen in de laadbewerking

- **bekijk omhoog het gebruikersprofiel in AEP**\
  Gebruik de ECID om te zoeken naar het gebruikersprofiel in Adobe Experience Platform. Dit helpt bevestigen dat de gebruiker wordt erkend en dat hun gegevens (zoals dupabonnement) correct worden opgeslagen.

- **verifieer de `price.drop` gebeurtenis wordt ontvangen**\
  Nadat u de gebeurtenis vanuit de webpagina hebt geactiveerd, checkt u AEP in of de gebeurtenis is ingevoegd en aan dezelfde ECID is gekoppeld.
Controleer de json van de message.feedback-gebeurtenis voor `feedback.status` . De statuswaarde moet `sent` zijn
  ![&#x200B; prijs-daling &#x200B;](assets/price-drop-profile-event.png)

- **bevestig dupberichten worden toegelaten**\
  Ervoor zorgen dat:
   - De gebruiker heeft de meldingsprompt van de browser geaccepteerd
   - Het profiel van de gebruiker bevat een pushtoken

- **Controle de reisopstelling**\
  Zorg ervoor dat de reis wordt gepubliceerd en geconfigureerd om naar de `price.drop` -gebeurtenis te luisteren.

