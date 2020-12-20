---
description: Attributo di configurazione per visualizzatore video per file multimediali diversi.
seo-description: Attributo di configurazione per visualizzatore video per file multimediali diversi.
seo-title: VideoPlayer.ssl
solution: Experience Manager
title: VideoPlayer.ssl
topic: Dynamic media
uuid: 07e2c55b-2388-44c8-83ab-338997c5cb71
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# VideoPlayer.ssl{#videoplayer-ssl}

Attributo di configurazione per visualizzatore video per file multimediali diversi.

>[!NOTE]
>
>Questo attributo di configurazione si applica solo a AEM 6.2 con installazione di [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) e a AEM 6.1 con installazione di [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Controlla se il video viene distribuito tramite una connessione SSL protetta (HTTPS) o una connessione non sicura (HTTP). </p> <p>Se impostato su <span class="codeph"> auto</span>, il protocollo di distribuzione video viene ereditato dal protocollo della pagina Web in cui è stato incorporato. Se la pagina Web viene caricata mediante HTTPS, il video viene distribuito anche attraverso HTTPS e viceversa. Se la pagina Web è su HTTP, il video viene distribuito su HTTP. </p> <p>Se è impostata su <span class="codeph"> su</span>, la distribuzione video avviene sempre su una connessione protetta, indipendentemente dal protocollo della pagina Web. </p> <p>Interessa solo la distribuzione di video pubblicati e viene ignorata per l’anteprima video in modalità Autore. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

Vedere anche [Secure Video Delivery](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb).
