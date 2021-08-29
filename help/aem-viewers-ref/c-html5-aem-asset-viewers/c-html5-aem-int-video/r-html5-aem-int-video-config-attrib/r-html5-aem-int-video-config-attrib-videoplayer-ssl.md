---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16e17e2f-be98-4a5a-ba5e-5d18e7f76fa4
source-git-commit: c58199c5884c368e92e50fe0ef9d6ad523e36266
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# VideoPlayer.ssl{#videoplayer-ssl}

Attributo di configurazione per Visualizzatore video interattivo.

<!-- >[!NOTE]
>
>This configuration attribute only applies to AEM 6.2 with installation of [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Controlla se il video viene distribuito tramite una connessione SSL protetta (HTTPS) o una connessione non sicura (HTTP). </p> <p>Se è impostato su <span class="codeph"> auto</span> il protocollo di consegna video viene ereditato dal protocollo della pagina web in cui è incorporato. Se la pagina web viene caricata su HTTPS, il video viene distribuito anche su HTTPS e viceversa. Se la pagina web è su HTTP, il video viene distribuito via HTTP. </p> <p>Se è impostato su <span class="codeph"> su</span>, la distribuzione video si verifica sempre su una connessione sicura, senza tenere conto del protocollo della pagina web. </p> <p>Influisce solo sulla distribuzione video pubblicata e viene ignorata per l’anteprima video in modalità Creazione. </p> </td> 
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

Vedere anche [Distribuzione video sicura](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
