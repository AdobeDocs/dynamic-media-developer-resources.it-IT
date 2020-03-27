---
description: 'null'
seo-description: 'null'
seo-title: Distribuzione video HTTPS
solution: Experience Manager
title: Distribuzione video HTTPS
topic: Dynamic media
uuid: 7f8c1fe6-b464-4d80-9ffe-a36081825d49
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365

---


# Distribuzione video HTTPS{#https-video-delivery}

>[!NOTE]
>
>La distribuzione sicura dei video si applica solo ad AEM 6.2 con l&#39;installazione di [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) e ad AEM 6.1 con l&#39;installazione di [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

A condizione che il visualizzatore funzioni nella configurazione come descritto all’inizio di questa sezione, la distribuzione video pubblicata può avvenire sia in modalità HTTPS (protetta) che HTTP (non sicura). In una configurazione predefinita, il protocollo di distribuzione video segue rigorosamente il protocollo di distribuzione della pagina Web in cui è stato incorporato. Tuttavia, è possibile imporre la distribuzione di video HTTPS senza tener conto del protocollo utilizzato dall&#39;incorporazione della pagina Web utilizzando l&#39;attributo di configurazione [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) . L’anteprima video in modalità Autore viene sempre trasmessa in modo protetto tramite HTTPS.

A seconda del metodo di pubblicazione di video per contenuti multimediali dinamici utilizzato in AEM, l’attributo di `VideoPlayer.ssl` configurazione viene applicato in modo diverso, come illustrato di seguito:

* Se pubblicate un video per contenuti multimediali dinamici con un URL, aggiungete `VideoPlayer.ssl` l’URL. Ad esempio, per forzare la distribuzione sicura dei video, aggiungete `&VideoPlayer.ssl=on` alla fine del seguente esempio di URL visualizzatore:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   See also [(Linking URLs to your Web Application](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Se pubblicate un video per contenuti multimediali dinamici con codice da incorporare, aggiungete `VideoPlayer.ssl` all’elenco di altri parametri di configurazione del visualizzatore presente nel frammento di codice da incorporare. Ad esempio, per imporre la distribuzione di video HTTPS, aggiungete `&VideoPlayer.ssl=on` come nell&#39;esempio seguente:

   ```
   <style type="text/css"> 
    #s7mixedmedia_div.s7mixedmediaviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/MixedMediaViewer.js"></script> 
   <div id="s7mixedmedia_div"></div> 
   <script type="text/javascript"> 
    var s7mixedmediaviewer = new s7viewers.MixedMediaViewer({ 
     "containerId" : "s7mixedmedia_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/MixedMedia_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "asset" : "/content/dam/Geometrixx-Outdoors-New-Launch/backpack/backpack_mixed_media" } 
    }).init(); 
   </script>
   ```

   See also [(Embedding the Video on a Web Page](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

