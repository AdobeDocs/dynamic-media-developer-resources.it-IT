---
description: Distribuzione video HTTPS
solution: Experience Manager
title: Distribuzione video HTTPS
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# Distribuzione video HTTPS{#https-video-delivery}

>[!NOTE]
>
>La distribuzione video sicura si applica solo a AEM 6.2 con l&#39;installazione di [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) e a AEM 6.1 con l&#39;installazione di [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

A condizione che il visualizzatore funzioni nella configurazione come descritto all’inizio di questa sezione, la distribuzione video pubblicata può avvenire sia in modalità HTTPS (protetta) che HTTP (non protetta). In una configurazione predefinita, il protocollo di consegna video segue rigorosamente il protocollo di consegna della pagina web di incorporamento. Tuttavia, è possibile forzare la distribuzione video HTTPS senza tenere conto del protocollo utilizzato incorporando la pagina web utilizzando l&#39;attributo di configurazione [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e) . L’anteprima video in modalità Autore viene sempre distribuita in modo sicuro tramite HTTPS.

A seconda del metodo di pubblicazione del video Dynamic Media utilizzato in AEM, l’attributo di configurazione `VideoPlayer.ssl` viene applicato in modo diverso, come illustrato di seguito:

* Se pubblichi un video Dynamic Media con un URL, aggiungi `VideoPlayer.ssl` all’URL. Ad esempio, per forzare la distribuzione video sicura, aggiungi `&VideoPlayer.ssl=on` alla fine del seguente esempio di URL visualizzatore:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
   ```

   Vedere anche [(Collegamento di URL all&#39;applicazione Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Se pubblichi un video Dynamic Media con codice da incorporare, aggiungi `VideoPlayer.ssl` all’elenco degli altri parametri di configurazione del visualizzatore nello snippet di codice da incorporare. Ad esempio, per forzare la distribuzione video HTTPS, aggiungi `&VideoPlayer.ssl=on` come nell’esempio seguente:

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

   Vedere anche [(Incorporare il video in una pagina web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic).
