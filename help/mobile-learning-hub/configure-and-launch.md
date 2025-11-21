---
title: Configureren en starten
description: Configureer de mobiele kanalen in Adobe Journey Optimizer (AJO) en Adobe Experience Platform (AEP), integreer met mobiele apps en zorg ervoor dat u klaar bent voor de uitvoering van de marketingcampagne.
feature: Overview
role: Developer, Admin
level: Beginner, Intermediate
hide: true
index: false
last-substantial-update: 2025-08-22T00:00:00Z
exl-id: d8ffe406-b54b-455f-bd41-7d1fef0a4714
source-git-commit: d892f1115045e5bd1cc89dc75e34434b9b5954bd
workflow-type: tm+mt
source-wordcount: '2561'
ht-degree: 0%

---


# Configureren en starten

Configureer de mobiele kanalen in Adobe Journey Optimizer en Adobe Experience Platform, integreer deze met mobiele apps en zorg ervoor dat u klaar bent voor het uitvoeren van de marketingcampagne.

>[!NOTE]
>
> Als u nog niet eerder in Journey Optimizer en Experience Platform werkt, dient u zich vertrouwd te maken met de kernbegrippen gegevensbeheer in Journey Optimizer door deze cursus te volgen:
>
> [ Gegevens van de ingenieur voor Intelligente Activering van de Reis in Adobe Journey Optimizer ](https://experienceleague.adobe.com/en/courses/ajo-engineer-data-for-intelligent-journey-activation){target="_blank"}
>*Leer hoe u realtime klantprofielgegevens voor Journey Optimizer instelt en beheert met Experience Platform. Begrijp gegevensmodellering, identiteitstoewijzing, en gegevensopname om verenigde profielen voor gepersonaliseerde klantenreizen tot stand te brengen.*


## Mobiele mogelijkheden in Adobe Journey Optimizer

Begrijp welke mobiele mogelijkheden Adobe Journey Optimizer biedt aan ontwikkelaars, marketers, en productteams, met inbegrip van duw overseinen, in-app overseinen, en inhoudpersonalisatie.

>[!VIDEO](https://video.tv.adobe.com/v/342103?quality=12&learn=on){transcript=true}


## Mobiele SDK en toepassingsconfiguratie

De mobiele implementaties in Journey Optimizer beginnen met de **Mobiele SDK van Adobe Experience Platform** integratie in uw app. SDK&#39;s zijn essentieel voor gegevensverzameling en interactie met Adobe Experience Platform (AEP) en de toepassingen ervan, zoals Adobe Journey Optimizer (AJO).

De mobiele SDK:

- Verzamelt app gebeurtenissen (het schermmeningen, tikken, aankopen, levenscyclusgebeurtenissen, enz.) en verzendt hen naar **Adobe Experience Platform Edge Network**.
- Beheert **identiteit** en **toestemming**, zodat kan Journey Optimizer klantenprofielen veilig bouwen en gebruiken.
- Registreert en werkt **pushtokens** bij, en verzendt **duw en in-app het volgen gebeurtenissen** terug naar Adobe Experience Platform.
- Integreert met **Journey Optimizer mobiele uitbreidingen** (duw, in-app, inhoudskaarten, besluitvorming) zodat de berichten kunnen worden geleverd, worden teruggegeven, en worden gemeten eind-aan-eind.

Zonder de Mobile SDK-integratie in uw app kan Journey Optimizer niet betrouwbaar zijn:

- Mobiele push- en in-app berichten leveren en bijhouden.
- Inhoudskaarten renderen en bijhouden.
- Gebruik real-time gedrag in de app om reizen te starten en ervaringen te personaliseren.


>[!PREREQUISITES]
>
>Zorg ervoor u hebt:
>
> - Adobe Journey Optimizer (AJO) is ingericht voor uw organisatie.
> - Adobe Experience Platform toegang met de toestemmingen van de Inzameling van Gegevens en Journey Optimizer.
> - Admin rights in AJO for channel and configuration setup.
> - Toegang tot de broncode van uw mobiele app (iOS, Android of het raamwerk voor verschillende platforms).
> - Uw app heeft de vereiste mogelijkheden op besturingssysteemniveau ingeschakeld (bijvoorbeeld pushmachtigingen, extensies voor meldingsservices en achtergrondmodi).


### Vereiste mobiele SDK-componenten voor Journey Optimizer

Om Journey Optimizer mobiele kanalen (duw, in-app, inhoudskaarten, op code-gebaseerde ervaringen) te gebruiken, moet u een reeks **kern** en **kanaal-specifieke** uitbreidingen in uw mobiele app installeren en vormen:

>[!BEGINTABS]

>[!TAB  Kern ]

#### Kernextensies (vereist voor alle mobiele toepassingen)

| Doel | Voorbeelden van extensies (iOS/Android) | Notities |
|----------------------|-----------------------------------------------|-------|
| Gebeurtenishub en -services | Mobile Core / AEP Core, AEP Services | Foundation for all other extensions. Verstrekt gebeurtenishub, voorzien van een netwerk, opslag, en gedeelde staat. |
| Edge Network | Adobe Experience Platform Edge Network | Verzendt toepassingsgebeurtenissen naar de Adobe Experience Platform Edge Network. |
| Identiteit | Identiteit voor Edge Network | Beheert ECID en andere identiteiten die voor profiel en segmentatie worden gebruikt. |
| Toestemming | Goedkeuring voor Edge Network | Verzamelt en dwingt de voorkeur van de gebruikerstoestemming af. |
| Assurance | Adobe Experience Platform Assurance | Gebruikt om SDK en kanaalconfiguratie van begin tot eind te bevestigen en te zuiveren. |

>[!TAB  kanaal-specifiek ]

#### Kanaalspecifieke extensies voor Journey Optimizer

| Kanaal/mogelijkheid | Extra belangrijke uitbreidingen (bovenop kern) | Wat ze mogelijk maken |
|------------------------|---------------------------------------------------------------------|------------------|
| Pushmeldingen | Journey Optimizer Mobile-extensie (push) | Registreer en werk duptokens bij, verzend dupvolgende gebeurtenissen, verbind met de dupconfiguratie van AJO. |
| In-app berichten | Journey Optimizer Mobile-extensie (in-app), UI-componenten voor berichten | In-app berichten in context ophalen en weergeven, impressies en interactiegebeurtenissen verzenden. |
| Inhoudskaarten | SDK berichten met ondersteuning voor inhoudskaarten | Ophalen, renderen en traceren van inhoudskaarten voor nauwkeurige Journey Optimizer-rapportage. |
| Ervaringen op basis van code | Journey Optimizer/beslissingsextensies of Edge Server-API | Besluiten nemen over specifieke &quot;oppervlakken&quot; in uw app. Uw app bepaalt hoe inhoud wordt weergegeven. |

>[!ENDTABS]

#### Eigenschappen en configuratie van mobiele tags

U vormt deze uitbreidingen in a **[mobiel markeringsbezit ](https://developer.adobe.com/client-sdks/home/getting-started/create-a-mobile-property/){target="_blank"}** in de Inzameling van Gegevens van AEP -> Markeringen.

This property controls:

- Welke mobiele SDK-extensies zijn geïnstalleerd.
- Welke gebeurtenissen in uw app oproepen naar de Edge Network activeren.
- Hoe gegevens worden toegewezen aan XDM en worden doorgestuurd naar Adobe-oplossingen (Journey Optimizer, Analytics, enz.).

U kunt [ tot stand brengen en dit mobiele bezit vormen manueel ](https://experienceleague.adobe.com/en/docs/platform-learn/data-collection/tags/create-a-property){target="_blank"}, of voor Mobiele In-App en Duw u de **[Geleide Opstelling van het Kanaal ](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup){target="_blank"}** kunt gebruiken om het vereiste markeringsbezit, datastream, en kanaalconfiguratie voor iOS en Android auto-tot stand te brengen.

>[!TIP]
>  
> Voor nieuwe implementaties, **[Geleide Opstelling van het Kanaal ](https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup){target="_blank"}** is het geadviseerde uitgangspunt. Het vermindert het risico van verkeerd gevormde gegevensstromen of ontbrekende uitbreidingen en loopt u door de bevestiging van SDK met Assurance.

#### Ga aan de slag met de Mobile SDK:

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/platform-learn/data-collection/mobile-sdk/overview
    {description = Learn how Adobe Experience Platform Mobile SDK powers end-to-end engagement in your mobile applications.}
* https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Platform Mobile SDK overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/platform-learn/data-collection/mobile-sdk/overview" title="Adobe Experience Platform Mobile SDK - overzicht" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/28948?format=jpeg&nocache=1763661968458" alt="Adobe Experience Platform Mobile SDK - overzicht"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/platform-learn/data-collection/mobile-sdk/overview" target="_blank" rel="referrer" title="Adobe Experience Platform Mobile SDK - overzicht"> Adobe Experience Platform Mobile SDK overzicht </a>
                    </p>
                    <p class="is-size-6">Leer hoe Adobe Experience Platform Mobile SDK de volledige betrokkenheid bij uw mobiele toepassingen mogelijk maakt.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/platform-learn/data-collection/mobile-sdk/overview" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Implement Adobe Experience Cloud in mobile apps tutorial">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" title="Zelfstudie Adobe Experience Cloud implementeren in mobiele apps" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview./media_1c75750ec1be623e56a379ca69ef6c495799e52a5.png?width=400&format=png&optimize=medium" alt="Zelfstudie Adobe Experience Cloud implementeren in mobiele apps"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" target="_blank" rel="referrer" title="Zelfstudie Adobe Experience Cloud implementeren in mobiele apps"> voer Adobe Experience Cloud in mobiele apps leerprogramma uit </a>
                    </p>
                    <p class="is-size-6">Leer hoe u de mobiele Adobe Experience Cloud-toepassingen implementeert. Deze zelfstudie begeleidt u door een implementatie van Experience Cloud-toepassingen in een voorbeeld van een Swift- of Android-app.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

#### Referenties ontwikkelaar:

<!-- CARDS
* https://developer.adobe.com/client-sdks/home/
* https://developer.adobe.com/client-sdks/home/current-sdk-versions/
* https://developer.adobe.com/client-sdks/home/getting-started/create-a-mobile-property/
* https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk/
* https://developer.adobe.com/client-sdks/home/getting-started/track-events/
* https://developer.adobe.com/client-sdks/home/base/assurance/
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Mobile SDK overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/" title="Overzicht van Mobile SDK" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Overzicht van Mobile SDK"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/" target="_blank" rel="referrer" title="Overzicht van Mobile SDK"> Mobiele SDK overzicht </a>
                    </p>
                    <p class="is-size-6">De overzichtspagina voor de documentatie van Adobe Experience Platform Mobile SDK.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Current SDK versions">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" title="Huidige SDK-versies" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Huidige SDK-versies"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank" rel="referrer" title="Huidige SDK-versies"> Huidige versies van SDK </a>
                    </p>
                    <p class="is-size-6">Een overzicht met de momenteel beschikbare mobiele extensies, samen met de versies, voor elk platform.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up a mobile property">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/getting-started/create-a-mobile-property/" title="Een mobiele eigenschap instellen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Een mobiele eigenschap instellen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/getting-started/create-a-mobile-property/" target="_blank" rel="referrer" title="Een mobiele eigenschap instellen"> Opstelling een mobiel bezit </a>
                    </p>
                    <p class="is-size-6">Een gids die verklaart hoe te opstelling een mobiel bezit, door het bezit te creëren, uitbreidingen te installeren, en de configuratie te publiceren. Als u dit proces voltooit, kunt u Mobile SDK gebruiken.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/getting-started/create-a-mobile-property/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Get the Adobe Experience Platform Mobile SDK">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk/" title="De Adobe Experience Platform Mobile SDK ophalen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="De Adobe Experience Platform Mobile SDK ophalen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk/" target="_blank" rel="referrer" title="De Adobe Experience Platform Mobile SDK ophalen"> krijgt de Mobiele SDK van Adobe Experience Platform </a>
                    </p>
                    <p class="is-size-6">Een handleiding voor het installeren van de Adobe Experience Platform Mobile SDK in uw toepassing.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Track events">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/getting-started/track-events/" title="Gebeurtenissen bijhouden" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Gebeurtenissen bijhouden"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/getting-started/track-events/" target="_blank" rel="referrer" title="Gebeurtenissen bijhouden"> gebeurtenissen van het Spoor </a>
                    </p>
                    <p class="is-size-6">Een handleiding voor het bijhouden van gebeurtenissen met Adobe Experience Platform Mobile SDK.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/getting-started/track-events/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Platform Assurance overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/base/assurance/" title="Adobe Experience Platform Assurance-overzicht" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Adobe Experience Platform Assurance-overzicht"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/base/assurance/" target="_blank" rel="referrer" title="Adobe Experience Platform Assurance-overzicht"> overzicht van Adobe Experience Platform Assurance </a>
                    </p>
                    <p class="is-size-6">Een overzicht voor de mobiele Adobe Experience Platform Assurance-extensie.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/base/assurance/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

>[!SUCCESS]
>
>**Mobiele SDK bereidheid checklist**
>
> [ ] Core SDK is geïnstalleerd (Core, Edge, Identity, Consent, Assurance).
> [ ] Mobiele Journey Optimizer-extensies toegevoegd voor de kanalen die u wilt gebruiken (push, in-app, inhoudskaarten, op code gebaseerd).
> [ ] DataStream correct geconfigureerd voor gebeurtenis- en profielgegevenssets.
> [ ] Identiteit en instemming geïmplementeerd en gevalideerd met Assurance.
> [ ] Registratie en reeksregistratie voor pushtoken die zijn gevalideerd.
> [ ] In-app en/of inhoudskaarten worden gevalideerd op een apparaat weergegeven.
> [ ] De Begeleide Opstelling van het Kanaal die voor nieuwe implementaties wordt gebruikt, of configuratie manueel gericht aan de gedocumenteerde stappen.


## Adobe Journey Optimizer Channel-configuratie

### In-app, Push en WhatsApp

Vorm uw **mobiele kanalen** gebruikend de geleide functionaliteit van de kanaalopstelling. Begrijp hoe te om het **WhatsApp kanaal** te vormen:

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup
 {description = Learn how to quickly set up and validate web and mobile channels across Experience Platform, Journey Optimizer, and Data Collection, and configure a push notification for a sample iOS marketing app.}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Guided channel setup">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup" title="Kanaalinstellingen met instructies" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3433053/?format=jpeg&nocache=1763661970550" alt="Kanaalinstellingen met instructies"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup" target="_blank" rel="referrer" title="Kanaalinstellingen met instructies"> Geleide kanaalopstelling </a>
                    </p>
                    <p class="is-size-6">Leer hoe u snel web- en mobiele kanalen in Experience Platform, Journey Optimizer en Gegevensverzameling instelt en valideert en een pushmelding configureert voor een voorbeeld van een iOS-marketingapp.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/web-and-mobile-channels/guided-channel-setup" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up the WhatsApp channel">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" title="Het WhatsApp-kanaal instellen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3470268/?format=jpeg&nocache=1763661970579" alt="Het WhatsApp-kanaal instellen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" target="_blank" rel="referrer" title="Het WhatsApp-kanaal instellen"> Opstelling het kanaal WhatsApp </a>
                    </p>
                    <p class="is-size-6">Dit leerprogramma begeleidt u door vestiging het WhatsApp kanaal in Adobe Journey Optimizer om bedrijfsoverseinen in real time toe te laten.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### SMS/MMS/RCS

Vorm **SMS/MMS/RCS kanalen** met de standaardleveranciers (Twilio, Synch of Infobip) of het gebruiken van een leverancier van douaneSMS:

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider
{description = Learn how to configure custom SMS providers in Journey Optimizer, set up API credentials and webhooks, manage opt-in/opt-out keywords, and launch personalized campaigns.}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure SMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" title="SMS API-referenties en kanaaloppervlakken configureren" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3413355?format=jpeg&nocache=1763661971419" alt="SMS API-referenties en kanaaloppervlakken configureren"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" target="_blank" rel="referrer" title="SMS API-referenties en kanaaloppervlakken configureren"> vorm de geloofsbrieven van SMS API en kanaaloppervlakken </a>
                    </p>
                    <p class="is-size-6">Leer hoe u Journey Optimizer kunt verbinden met een SMS-serviceprovider en hoe u een SMS-kanaaloppervlak kunt maken.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure a custom SMS provider">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" title="Een aangepaste SMS-provider configureren" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3431625/?format=jpeg&nocache=1763661971435" alt="Een aangepaste SMS-provider configureren"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" target="_blank" rel="referrer" title="Een aangepaste SMS-provider configureren"> vorm een leverancier van douaneSMS </a>
                    </p>
                    <p class="is-size-6">Leer hoe u aangepaste SMS-providers in Journey Optimizer configureert, API-referenties en -websites instelt, sleutelwoorden voor aanmelding/opt-out beheert en gepersonaliseerde campagnes start.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure MMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" title="MMS API-referenties en kanaaloppervlakken configureren" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3428872/?format=jpeg&nocache=1763661971338" alt="MMS API-referenties en kanaaloppervlakken configureren"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" target="_blank" rel="referrer" title="MMS API-referenties en kanaaloppervlakken configureren"> vorm MMS API geloofsbrieven en kanaaloppervlakken </a>
                    </p>
                    <p class="is-size-6">Leer hoe u Journey Optimizer kunt verbinden met een MMS-serviceprovider en hoe u een MMS-kanaaloppervlak kunt maken.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up RCS in Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" title="RCS instellen in Journey Optimizer" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3464755/?format=jpeg&nocache=1763661971296" alt="RCS instellen in Journey Optimizer"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" target="_blank" rel="referrer" title="RCS instellen in Journey Optimizer"> opstelling RCS in Journey Optimizer </a>
                    </p>
                    <p class="is-size-6">Leer hoe u merkgebonden, interactieve RCS-berichten in Adobe Journey Optimizer configureert en verzendt met een aangepaste SMS-provider. Deze zelfstudie doorloopt het instellen van API-referenties, webhooks en kanaalconfiguraties en bouwt vervolgens een reis om rijke, gepersonaliseerde berichtenervaringen te bieden - allemaal binnen de native messaging-app.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Naleving van privacywetten en platformrichtlijnen garanderen.

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page{image=../mobile-learning-hub/assets/privacy.webp}{title = Privacy Features in Adobe Journey Optimizer}{description = Learn how to process privacy requests, audit user actions, manage consent, apply governance rules, and leverage advanced security options like Customer Managed Keys.}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables{cta = Watch}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Privacy Features in Adobe Journey Optimizer">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" title="Privacy-functies in Adobe Journey Optimizer" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../mobile-learning-hub/assets/privacy.webp" alt="Privacy-functies in Adobe Journey Optimizer"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" target="_blank" rel="referrer" title="Privacy-functies in Adobe Journey Optimizer"> Eigenschappen van de Privacy in Adobe Journey Optimizer </a>
                    </p>
                    <p class="is-size-6">Leer hoe te om privacyverzoeken, controlegebruikersacties te verwerken, toestemming te beheren, beheersregels toe te passen, en hefboomwerking geavanceerde veiligheidsopties zoals KlantBeheerde Sleutels.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Data Governance Framework Overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" title="Overzicht van het gegevensbeheerframework" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/29708/?format=jpeg&nocache=1763661972554" alt="Overzicht van het gegevensbeheerframework"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" target="_blank" rel="referrer" title="Overzicht van het gegevensbeheerframework"> Overzicht van het Kader van het Kader van het Beheer van Gegevens </a>
                    </p>
                    <p class="is-size-6">Begrijp de bestuurskenmerken in Adobe Experience Platform.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Classify data using labels">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" title="Gegevens classificeren met labels" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/29709?format=jpeg&nocache=1763661972557" alt="Gegevens classificeren met labels"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" target="_blank" rel="referrer" title="Gegevens classificeren met labels"> classificeer gegevens gebruikend etiketten </a>
                    </p>
                    <p class="is-size-6">Leer hoe te om etiketten op uw schema's en datasets toe te passen.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Create Data Usage Policies">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" title="Beleid voor gegevensgebruik maken" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/32977/?format=jpeg&nocache=1763661972555" alt="Beleid voor gegevensgebruik maken"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" target="_blank" rel="referrer" title="Beleid voor gegevensgebruik maken"> creeer het Beleid van het Gebruik van Gegevens </a>
                    </p>
                    <p class="is-size-6">Leer hoe u beleid voor gegevensgebruik maakt en beheert.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Controle </span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Gemeenschappelijke uitvoeringsvalkuilen en hoe deze te vermijden

De meeste mobiele kwesties komen uit **SDK of configuratie van de gegevensinzameling**, niet in de reizen of campagnes van Journey Optimizer zelf voort. Gebruik de onderstaande tabel om te bepalen wat er mis gaat en vouw vervolgens de bijbehorende sectie uit voor meer informatie.

### Beknopte piek

| Aantal | Probleem/symptoom | Veelvoorkomende fout | In één oogopslag corrigeren |
|---|----------------------------------------------|-----------------------------------------------------|------------------------------------------|
| 1 | De Begeleide Opstelling van het Kanaal ontbreekt; geen of laag verkeer | [ niet uitgelijnde versies of uitbreidingen van SDK ](#1-sdk-versions-and-extensions-not-aligned-with-channel-requirements) | SDK/extensie-versies bijwerken; valideren in Assurance |
| 2 | Batch bijhouden mislukt; fouten in AEP | [ Gegevensstromen of datasets misconfigured ](#2-misconfigured-datastreams-or-datasets) | Gebeurtenissen toewijzen aan gegevensset en profielen voor gebeurtenissen aan profielgegevensset |
| 3 | Reizen branden niet; oneven personalisatie | [ Ontbrekende of inconsistente Identiteit of toestemming ](#3-missing-or-inconsistent-identity-and-consent) | Edge-identiteit en -toestemming implementeren; verifiëren in Assurance |
| 4 | Geen push-levering of wordt geopend in rapporten | [ de symbolische registratie of het volgen gebroken ](#4-push-token-registration-and-tracking-not-wired-correctly) | Symboolregistratie en -interactietracering corrigeren via SDK |
| 5 | Geen impressies in de app ondanks actieve campagnes | [ In-app berichten of inhoudskaarten die ](#5-in-app-messages-or-content-cards-not-displaying) niet tonen | Berichtextensies, triggers en Assurance-beslissingsreacties controleren |

### Gedetailleerde richtsnoeren per toonhoogte

Open de valhoogte die overeenkomt met uw symptomen om te zien wat u moet controleren en hoe u deze kunt corrigeren.

<details id="1-sdk-versions-and-extensions-not-aligned-with-channel-requirements">
<summary><strong>1. SDK-versies en -extensies die niet zijn uitgelijnd met kanaalvereisten </strong></summary>

**wat u** zult opmerken

- Duw- of in-app-activiteiten bereiken het apparaat niet.
- De instelling van kanalen met instructies of de kanaalvalidatie is mislukt.
- In Assurance worden ontbrekende Journey Optimizer-, Edge- of Identity-extensies weergegeven.

**wat te controleren**

- Gebruikt u de minimum **Mobiele Kern** en **Journey Optimizer** uitbreidingsversies die door Geleide Opstelling van het Kanaal worden vereist?
- In **Assurance**, onder uitbreidingen en gebeurtenissen:
   - Ziet u de verwachte geladen extensies?
   - Worden de gebeurtenissen naar de Edge Network gestuurd en erkend?

**hoe te om** te bevestigen

- Voer een upgrade uit naar de ondersteunde Mobile SDK- en Journey Optimizer-extensieversies.
- Maak de app opnieuw, maak opnieuw verbinding met Assurance en voer de instelling van het geleide kanaal opnieuw uit.

Zie: [ Opstelling mobiel en Web ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config){target="_blank"}

</details>


<details id="2-misconfigured-datastreams-or-datasets">
<summary><strong> 2. Misconfigured gegevensstromen of datasets </strong></summary>

**wat u** zult opmerken

- Gebeurtenissen of batches voor het bijhouden van push-gegevens mislukken in de gegevenssets van het platform.
- Fouten bij het invoeren van gegevens (updates worden bijvoorbeeld niet ondersteund voor gebeurtenissen).
- In pushrapporten of in-app-rapporten wordt weinig of geen tracking getoond.

**wat te controleren**

- Heeft iemand **systeemschema&#39;s of datasets** veranderd die voor het volgen van Journey Optimizer worden gecreeerd?
- In uw **datastream**:
   - Zijn ervaringsgebeurtenissen in kaart gebracht aan een **gebeurtenisdataset**?
   - Zijn profielattributen in kaart gebracht aan a **profieldataset**?

**hoe te om** te bevestigen

- Bewerk geen systeemdatasets/schema&#39;s die door AJO zijn gemaakt.
- Corrigeer de gegevenstoewijzing (events → gebeurtenisdataset, profielen → profieldataset).
- Voorkeur voor de instelling met instructies voor Kanaal of de gedocumenteerde gegevensstroomstappen in plaats van ad-hocwijzigingen.

Zie: [ de stroom van het Bericht van de duw in Adobe Journey Optimizer ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

</details>


<details id="3-missing-or-inconsistent-identity-and-consent">
<summary><strong> 3. Ontbrekende of inconsistente identiteit en toestemming </strong></summary>

**wat u** zult opmerken

- Reizen worden niet geactiveerd zoals verwacht voor gebruikers van de app.
- Personalization komt niet overeen met het gedrag van de gebruiker op andere kanalen.
- Gebeurtenissen worden weergegeven in Experience Platform, maar profielen zien er gefragmenteerd uit.

**wat te controleren**

- Is **Identiteit voor Edge Network** uitgevoerd en verzendend een stabiele primaire identiteitskaart (bijvoorbeeld, login identiteitskaart)?
- Is **Toestemming voor Edge Network** uitgevoerd en bijgewerkt wanneer voorkeur verandert?
- In **Assurance**:
   - Omvatten uitgaande gebeurtenissen toestemmingswaarden?
   - Neemt u de ECID en uw primaire id&#39;s consistent op?

**hoe te om** te bevestigen

- Voer of verbeter **Identiteit voor Edge Network** in app uit.
- Voer **Toestemming voor Edge Network** uit en verbind het met de toestemmings UI van uw app.
- Herstel in Assurance totdat de identiteit en toestemming voor alle relevante gebeurtenissen worden weergegeven.

Zie: [ voer toestemming voor de implementaties van SDK van het Platform Mobiele uit ](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent){target="_blank"}

</details>


<details id="4-push-token-registration-and-tracking-not-wired-correctly">
<summary><strong> 4. Registratie en tekstspatiëring van pushtoken zijn niet correct bekabeld </strong></summary>

**wat u** zult opmerken

- Gebruikers ontvangen nooit pushmeldingen, ook al worden campagnes of reizen uitgevoerd.
- In pushrapporten worden geen bewerkingen, dissen of interacties weergegeven.

**wat te controleren**

- Registreert de app het pushtoken met de Journey Optimizer-extensie:
   - Bij de eerste installatie?
   - Na elke update van de app?
   - Wanneer het besturingssysteem het token vernieuwt?
- Wanneer een gebruiker een bericht opent of ontkent, ziet u het volgen gebeurtenissen in Assurance?

**hoe te om** te bevestigen

- Voeg de code toe of verbeter de code die:
   - Registreert het token via de mobiele Journey Optimizer-extensie wanneer het wordt gemaakt of vernieuwd.
   - Verzendt pushinteractiegebeurtenissen (open, negeren, aangepaste handelingen) via de Mobile SDK.
- Gebruik Assurance om te bevestigen dat registratie- en volggebeurtenissen plaatsvinden zoals u had verwacht.

Zie: [ de stroom van het Bericht van de duw in Adobe Journey Optimizer ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

</details>


<details id="5-in-app-messages-or-content-cards-not-displaying">
<summary><strong> 5. In-app berichten of inhoudskaarten die niet worden weergegeven </strong></summary>

**wat u** zult opmerken

- In-app berichten of inhoudskaarten worden nooit weergegeven, ondanks actieve campagnes of reizen.
- Bij rapportage worden 0 afbeeldingen weergegeven.

**wat te controleren**

- Zijn het **mobiele overseinen van Journey Optimizer / in-app uitbreiding** en **Overseinen SDK** geïnstalleerd en geregistreerd in app?
- In uw **markeringen** configuratie:
   - Hebt u regels die verzoeken om de juiste gebeurtenissen (bijvoorbeeld schermweergaven of aangepaste gebeurtenissen) activeren?
- In **Assurance**:
   - Wanneer deze gebeurtenissen plaatsvinden, ziet u verzoeken om een beslissing in de app of een inhoudskaart uit?
   - Ziet u reacties die terugkomen van de Edge Network?

**hoe te om** te bevestigen

- Installeer en registreer de vereiste overseinenuitbreidingen.
- Voeg of verbeter regels toe die besluiten over uw doelgebeurtenissen (schermen, douanegebeurtenissen) teweegbrengen.
- Voor inhoudskaarten dient u:
   - Fetch cards via de Messaging SDK API&#39;s.
   - Geef hen in uw UI terug.
   - Interacties via de SDK bijhouden.

Zie:
- [ creeer en verzend in-app berichten ](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/experience-cloud/journey-optimizer/journey-optimizer-inapp){target="_blank"}
- [ vorm de steun van inhoudskaarten in Mobiele SDK ](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp){target="_blank"}

</details>

>[!SUCCESS]
>
> **Één-lijn checklist van de gereedheid**
>
> Alvorens app aan marketers te verstrekken, bevestig in **[Assurance ](https://developer.adobe.com/client-sdks/home/base/assurance/){target="_blank"}** dat:
> 
> [ ] Core SDK + Journey Optimizer-extensies zijn geladen,\
> [ ] De gebeurtenissen stromen op de correcte gegevensstroom en datasets,\
> [ ] de identiteit en de toestemming zijn aanwezig op alle zeer belangrijke gebeurtenissen,\
> [ ] Er worden pushtokens en interacties bijgehouden, en\
> [ ] Ten minste één test in-app-bericht of inhoudskaart is weergegeven en opgenomen als een indruk.

## Blogberichten

- [ Gebruikend op CDN gebaseerde cliënt zijverpersoonlijking (ODD) op mobiel voor snellere verpersoonlijkingen.](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/using-cdn-based-client-side-personalization-odd-on-mobile-for/ba-p/761626){target="_blank"}
- [ Mobile Activation voor Adobe Experience Cloud ](https://experienceleaguecommunities.adobe.com/t5/adobe-target-blogs/mobile-activation-for-adobe-experience-cloud/ba-p/541595){target="_blank"}
