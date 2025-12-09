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
source-git-commit: 2b472e440ca12169bed22d1f99370f7a6b0a0bf8
workflow-type: tm+mt
source-wordcount: '2148'
ht-degree: 0%

---


# Configureren en starten

Voor **beheerders** en **mobiele app ontwikkelaars**, toont deze sectie hoe te om mobiele en Webkanalen in Adobe Journey Optimizer te vormen en te lanceren. Hieronder vindt u vereisten, machtigingen en platformondersteuning, en begeleidt u vervolgens bij het maken van toepassingsspecifieke configuraties.

>[!IMPORTANT]
>
> Als u aan Journey Optimizer en Experience Platform nieuw bent, vertrouwd me met het kernconcepten gegevensbeheer in Journey Optimizer door deze cursus te nemen: [&#x200B; Gegevens van de ingenieur voor Intelligente Activering van de Reis in Adobe Journey Optimizer &#x200B;](https://experienceleague.adobe.com/en/courses/ajo-engineer-data-for-intelligent-journey-activation){target="_blank"}
>


## Mobiele mogelijkheden in Adobe Journey Optimizer

Begrijp welke mobiele mogelijkheden Adobe Journey Optimizer biedt aan ontwikkelaars, marketers, en productteams, met inbegrip van duw overseinen, in-app overseinen, en inhoudpersonalisatie.

>[!VIDEO](https://video.tv.adobe.com/v/342103?quality=12&learn=on){transcript=true}


## Kanaalconfiguratie

### Mobiele push en in-app

De mobiele implementaties in Journey Optimizer beginnen met de **Mobiele SDK van Adobe Experience Platform** integratie in uw app. SDK&#39;s zijn essentieel voor gegevensverzameling en interactie met Adobe Experience Platform (AEP) en de toepassingen ervan, zoals Adobe Journey Optimizer (AJO).

#### Wat is de Mobile SDK?

De mobiele SDK:

- Verzamelt app gebeurtenissen (het schermmeningen, tikken, aankopen, levenscyclusgebeurtenissen, enz.) en verzendt hen naar **Adobe Experience Platform Edge Network**.
- Beheert **identiteit** en **toestemming**, zodat kan Journey Optimizer klantenprofielen veilig bouwen en gebruiken.
- Registreert en werkt **pushtokens** bij, en verzendt **duw en in-app het volgen gebeurtenissen** terug naar Adobe Experience Platform.
- Integreert met de **[mobiele uitbreiding van Journey Optimizer &#x200B;](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer)** zodat kunnen de berichten worden geleverd, worden teruggegeven, en gemeten van begin tot eind.

Zonder de Mobile SDK-integratie in uw app kan Journey Optimizer niet betrouwbaar zijn:

- Mobiele push- en in-app berichten leveren en bijhouden.
- Inhoudskaarten renderen en bijhouden.
- Gebruik real-time gedrag in de app om reizen te starten en ervaringen te personaliseren.

#### Kanaalinstellingen met instructies voor nieuwe implementaties

Voor nieuwe mobiele in-app en push-implementaties is de instelling van kanalen met instructies het aanbevolen beginpunt. Het vermindert het risico van verkeerd gevormde gegevensstromen of ontbrekende uitbreidingen en loopt u door de bevestiging van SDK met Assurance.

>[!PREREQUISITES]
>
>Zorg ervoor u hebt:
>
> - **Adobe Journey Optimizer** (AJO) provisioned voor uw org.
> - Adobe Experience Platform toegang met [&#x200B; de toestemmingen van de Inzameling van Gegevens en van Journey Optimizer &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config#:~:text=Required%20permissions).
> - Admin rights in AJO for channel and configuration setup.
> - Toegang tot de broncode van uw mobiele app (iOS, Android of het raamwerk voor verschillende platforms).
> - Uw app heeft de vereiste mogelijkheden op besturingssysteemniveau ingeschakeld (bijvoorbeeld pushmachtigingen, extensies voor meldingsservices en achtergrondmodi).
> - Als u de bestaande configuratieoptie gebruikt, gelieve ervoor te zorgen dat u de [&#x200B; huidige versies van Adobe Experience Platform Mobile SDK &#x200B;](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"} gebruikt


>[!VIDEO](https://video.tv.adobe.com/v/3433053/?learn=on)

Voor meer informatie zie [&#x200B; begonnen worden met geleide kanaalopstelling &#x200B;](https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config.html){target="_blank"}


#### Handmatige configuratie van het pushkanaal

In de volgende handleidingen vindt u alles wat u nodig hebt om pushberichten handmatig te configureren en te gebruiken, van inzicht in de gegevensstroom tot integratie met services zoals Firebase en Apple Push Notification Service (APN) tot het instellen van mobiele apps en testmeldingen.

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs
{title = Push notification data flow and components}
{description = Learn how to setup and understand key services and workflows involved with push notifications in Journey Optimizer.}
{image = https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1f6e99fa57e318230d92f5dde619c450690b5d27a.png?width=2000&format=webply&optimize=medium}
{target = _blank}

* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration
{image = https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1134ddf9b0f7d39bb365d4884a1d603fd4aa5bbdf.png?width=2000&format=webply&optimize=small}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/overview 
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Push notification data flow and components">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" title="Gegevensstroom van pushmeldingen en componenten" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1f6e99fa57e318230d92f5dde619c450690b5d27a.png?width=400&format=webply&optimize=medium" alt="Gegevensstroom van pushmeldingen en componenten"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" target="_blank" rel="referrer" title="Gegevensstroom van pushmeldingen en componenten"> de stroom van het pushbericht en componenten </a>
                    </p>
                    <p class="is-size-6">Leer hoe u belangrijke services en workflows voor pushberichten in Journey Optimizer instelt en begrijpt.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Push notification configuration">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" title="Configuratie van pushmeldingen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/media_1134ddf9b0f7d39bb365d4884a1d603fd4aa5bbdf.png?width=400&format=webply&optimize=small" alt="Configuratie van pushmeldingen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" target="_blank" rel="referrer" title="Configuratie van pushmeldingen"> Push berichtconfiguratie </a>
                    </p>
                    <p class="is-size-6">Leer hoe u uw omgeving configureert voor het verzenden van pushmeldingen met Journey Optimizer</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-configuration" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
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

#### Aanvullende bronnen


<!-- CARDS
* https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk
{target = _blank}
* https://developer.adobe.com/client-sdks/home/base/assurance
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Get the Adobe Experience Platform Mobile SDK">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" title="De Adobe Experience Platform Mobile SDK ophalen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="De Adobe Experience Platform Mobile SDK ophalen"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" target="_blank" rel="referrer" title="De Adobe Experience Platform Mobile SDK ophalen"> krijgt de Mobiele SDK van Adobe Experience Platform </a>
                    </p>
                    <p class="is-size-6">Een handleiding voor het installeren van de Adobe Experience Platform Mobile SDK in uw toepassing.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/getting-started/get-the-sdk" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Platform Assurance overview">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/client-sdks/home/base/assurance" title="Adobe Experience Platform Assurance-overzicht" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://developer.adobe.com/shared/images/adobe-social-share.png" alt="Adobe Experience Platform Assurance-overzicht"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/client-sdks/home/base/assurance" target="_blank" rel="referrer" title="Adobe Experience Platform Assurance-overzicht"> overzicht van Adobe Experience Platform Assurance </a>
                    </p>
                    <p class="is-size-6">Een overzicht voor de mobiele Adobe Experience Platform Assurance-extensie.</p>
                </div>
                <a href="https://developer.adobe.com/client-sdks/home/base/assurance" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

#### Controlelijst voor gereedheid voor mobiele SDK

Alvorens app aan marketers te verstrekken, bevestig in **[Assurance &#x200B;](https://developer.adobe.com/client-sdks/home/base/assurance/){target="_blank"}** dat:

>[!SUCCESS]
> 
> [ ] Core SDK + Journey Optimizer-extensies zijn geladen,\
> [ ] De gebeurtenissen stromen op de correcte gegevensstroom en datasets,\
> [ ] de identiteit en de toestemming zijn aanwezig op alle zeer belangrijke gebeurtenissen,\
> [ ] Er worden pushtokens en interacties bijgehouden, en\
> [ ] Ten minste één test in-app-bericht of inhoudskaart is weergegeven en opgenomen als een indruk.


### Inhoudskaarten

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp
{title = Configure content cards support in Mobile SDK}
{description = Learn how to integrate content cards in your mobile application using Messaging SDK.}
{image = https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/media_17623afb1c5e280b7fb6861b4003d0ef8f8bea24d.jpg?width=2000&format=webply&optimize=medium}
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure content cards support in Mobile SDK">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" title="Ondersteuning voor inhoudskaarten configureren in Mobile SDK" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/media_17623afb1c5e280b7fb6861b4003d0ef8f8bea24d.jpg?width=400&format=webply&optimize=medium" alt="Ondersteuning voor inhoudskaarten configureren in Mobile SDK"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" target="_blank" rel="referrer" title="Ondersteuning voor inhoudskaarten configureren in Mobile SDK"> vorm de steun van inhoudskaarten in Mobiele SDK </a>
                    </p>
                    <p class="is-size-6">Leer hoe u inhoudskaarten in uw mobiele toepassing integreert met Berichten SDK.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### WhatsApp

Begrijp hoe te om het **WhatsApp kanaal** te vormen:

<!-- CARDS
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Set up the WhatsApp channel">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/whatsapp-channel/set-up-whatsapp-channel" title="Het WhatsApp-kanaal instellen" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3470268/?format=jpeg&nocache=1765310599408" alt="Het WhatsApp-kanaal instellen"
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
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-custom-sms-provider
{description = Learn how to configure custom SMS providers in Journey Optimizer, set up API credentials and webhooks, manage opt-in/opt-out keywords, and launch personalized campaigns.}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/configure-mms-api-credentials-and-channel-surfaces
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-rcs
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Configure SMS API credentials and channel surfaces">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/sms-mms-channel/set-up-sms-channel" title="SMS API-referenties en kanaaloppervlakken configureren" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3413355?format=jpeg&nocache=1765310599850" alt="SMS API-referenties en kanaaloppervlakken configureren"
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
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3431625/?format=jpeg&nocache=1765310599834" alt="Een aangepaste SMS-provider configureren"
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
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3428872/?format=jpeg&nocache=1765310599863" alt="MMS API-referenties en kanaaloppervlakken configureren"
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
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/3464755/?format=jpeg&nocache=1765310600192" alt="RCS instellen in Journey Optimizer"
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
* https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent
* https://experienceleague.adobe.com/en/docs/journey-optimizer/using/privacy/privacy-landing-page{image=../mobile-learning-hub/assets/privacy.webp}{title = Privacy Features in Adobe Journey Optimizer}{description = Learn how to process privacy requests, audit user actions, manage consent, apply governance rules, and leverage advanced security options like Customer Managed Keys.}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/data-governance-framework
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/classify-data-using-lables
{cta = Watch}
{target = _blank}
* https://experienceleague.adobe.com/en/docs/journey-optimizer-learn/tutorials/data-governance-and-privacy/create-data-usage-policies
{target = _blank}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Implement consent for Platform Mobile SDK implementations">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent" title="Goedkeuring implementeren voor Platform Mobile SDK-implementaties" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent./media_12356d2400b5ad641e8356a6883441b38a129c968.png?width=400&format=png&optimize=medium" alt="Goedkeuring implementeren voor Platform Mobile SDK-implementaties"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent" target="_blank" rel="referrer" title="Goedkeuring implementeren voor Platform Mobile SDK-implementaties"> voer toestemming voor de implementaties van Platform Mobile SDK uit </a>
                    </p>
                    <p class="is-size-6">Leer hoe u toestemming implementeert in een mobiele app.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold"> Leer meer </span>
                </a>
            </div>
        </div>
    </div>
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
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/29708/?format=jpeg&nocache=1765310600883" alt="Overzicht van het gegevensbeheerframework"
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
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/29709?format=jpeg&nocache=1765310600887" alt="Gegevens classificeren met labels"
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
                        <img class="is-bordered-r-small" src="https://video.tv.adobe.com/v/32977/?format=jpeg&nocache=1765310600676" alt="Beleid voor gegevensgebruik maken"
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
| 1 | De Begeleide Opstelling van het Kanaal ontbreekt; geen of laag verkeer | [&#x200B; niet uitgelijnde versies of uitbreidingen van SDK &#x200B;](#1-sdk-versions-and-extensions-not-aligned-with-channel-requirements) | SDK/extensie-versies bijwerken; valideren in Assurance |
| 2 | Batch bijhouden mislukt; fouten in AEP | [&#x200B; Gegevensstromen of datasets misconfigured &#x200B;](#2-misconfigured-datastreams-or-datasets) | Gebeurtenissen toewijzen aan gegevensset en profielen voor gebeurtenissen aan profielgegevensset |
| 3 | Reizen branden niet; oneven personalisatie | [&#x200B; Ontbrekende of inconsistente Identiteit of toestemming &#x200B;](#3-missing-or-inconsistent-identity-and-consent) | Edge-identiteit en -toestemming implementeren; verifiëren in Assurance |
| 4 | Geen push-levering of wordt geopend in rapporten | [&#x200B; de symbolische registratie of het volgen gebroken &#x200B;](#4-push-token-registration-and-tracking-not-wired-correctly) | Symboolregistratie en -interactietracering corrigeren via SDK |
| 5 | Geen impressies in de app ondanks actieve campagnes | [&#x200B; In-app berichten of inhoudskaarten die &#x200B;](#5-in-app-messages-or-content-cards-not-displaying) niet tonen | Berichtextensies, triggers en Assurance-beslissingsreacties controleren |

### Gedetailleerde richtsnoeren per toonhoogte

Open de valhoogte die overeenkomt met uw symptomen om te zien wat u moet controleren en hoe u deze kunt corrigeren.

+++ &#x200B;1. SDK-versies en -extensies zijn niet uitgelijnd met kanaalvereisten
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

Zie: [&#x200B; Opstelling mobiel en Web &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/guided-setup/set-mobile-config){target="_blank"}

+++

+++ &#x200B;2. Verkeerde gegevensstromen of datasets
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

Zie: [&#x200B; de stroom van het Bericht van de duw in Adobe Journey Optimizer &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

+++

+++ &#x200B;3. Ontbrekende of inconsistente identiteit en toestemming
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

Zie: [&#x200B; voer toestemming voor de implementaties van SDK van het Platform Mobiele uit &#x200B;](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/consent){target="_blank"}

+++

+++ &#x200B;4. Registratie en tekstspatiëring van pushtoken is niet correct bekabeld
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

Zie: [&#x200B; de stroom van het Bericht van de duw in Adobe Journey Optimizer &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/push/push-config/push-gs){target="_blank"}

+++

+++ &#x200B;5. In-app berichten of inhoudskaarten worden niet weergegeven
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
- [&#x200B; creeer en verzend in-app berichten &#x200B;](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/experience-cloud/journey-optimizer/journey-optimizer-inapp){target="_blank"}
- [&#x200B; vorm de steun van inhoudskaarten in Mobiele SDK &#x200B;](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/content-card/configure/content-card-lp){target="_blank"}

+++

## Aanvullende bronnen

- [&#x200B; Gebruikend op CDN gebaseerde cliënt zijpersonalisatie (ODD) op mobiel voor snellere verpersoonlijkingen (Blog) &#x200B;](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/using-cdn-based-client-side-personalization-odd-on-mobile-for/ba-p/761626){target="_blank"}
- [&#x200B; Geheim aan Mobiele de Betrokkenheid en Groei van de Toepassing op het volgende niveau (de Zitting van de Top) &#x200B;](https://business.adobe.com/summit/2025/sessions/the-secret-to-nextlevel-mobile-app-engagement-s603.html)
