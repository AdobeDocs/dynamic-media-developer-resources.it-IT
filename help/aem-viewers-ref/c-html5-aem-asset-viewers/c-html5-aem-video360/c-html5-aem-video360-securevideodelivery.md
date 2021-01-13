---
description: Distribuzione video HTTPS
solution: Experience Manager
title: Distribuzione video HTTPS
topic: Dynamic media
uuid: 68984ba1-2802-496a-8ad0-ba46b59514ad
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Distribuzione video HTTPS{#https-video-delivery}

>[!NOTE]
>
>HTTP Secure Video Delivery si applica solo a AEM 6.2 con l&#39;installazione di [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) e a AEM 6.1 con l&#39;installazione di [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

A condizione che il visualizzatore funzioni nella configurazione come descritto all’inizio di questa sezione, la distribuzione video pubblicata può avvenire sia in modalità HTTPS (protetta) che HTTP (non sicura). In una configurazione predefinita, il protocollo di distribuzione video segue rigorosamente il protocollo di distribuzione della pagina Web in cui è stato incorporato. Tuttavia, è possibile imporre la distribuzione di video HTTPS senza tener conto del protocollo utilizzato dall&#39;incorporazione della pagina Web utilizzando l&#39;attributo di configurazione [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md). L’anteprima video in modalità Autore viene sempre trasmessa in modo protetto tramite HTTPS.

A seconda del metodo di pubblicazione del video Dynamic Media utilizzato in AEM, l&#39;attributo di configurazione `Video360Player.ssl` viene applicato in modo diverso, come illustrato di seguito:

* Se pubblicate un video Dynamic Media con un URL, aggiungete `Video360Player.ssl` all’URL. Ad esempio, per forzare la distribuzione sicura dei video, aggiungete `&Video360Player.ssl=on` alla fine del seguente esempio di URL visualizzatore:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   Vedere anche [Collegamento di URL all&#39;applicazione Web](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

* Se pubblicate un video Dynamic Media con codice da incorporare, aggiungete `Video360Player.ssl` all’elenco degli altri parametri di configurazione del visualizzatore nello snippet di codice da incorporare. Ad esempio, per imporre la distribuzione di video HTTPS, aggiungete `&Video360Player.ssl=on` come nell&#39;esempio seguente:

   ```
   <style type="text/css"> 
    #s7video_div.s7video360viewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js"></script> 
   <div id="s7video_div"></div> 
   <script type="text/javascript"> 
    var s7video360viewer = new s7viewers.Video360Viewer({ 
     "containerId" : "s7video_div", 
     "params" : {  
      "Video360Player.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Video", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "posterimage": "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }).init(); 
   </script>
   ```

   Vedere anche [Incorporazione del video in una pagina Web](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)

