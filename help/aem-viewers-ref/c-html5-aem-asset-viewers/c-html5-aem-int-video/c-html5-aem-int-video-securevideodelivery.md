---
description: 'null'
seo-description: 'null'
seo-title: Distribuzione video HTTPS
solution: Experience Manager
title: Distribuzione video HTTPS
topic: Dynamic media
uuid: acda9c8f-e8f4-4855-9b14-82838ec5a1b9
translation-type: tm+mt
source-git-commit: 6cff4553307fe6cbda4b80ce3f39b58e615fa365
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Distribuzione video HTTPS{#https-video-delivery}

>[!NOTE]
>
>La distribuzione sicura dei video si applica solo a AEM 6.2 con l&#39;installazione di [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) e a AEM 6.1 con l&#39;installazione di [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

A condizione che il visualizzatore funzioni nella configurazione come descritto all’inizio di questa sezione, la distribuzione video pubblicata può avvenire sia in modalità HTTPS (protetta) che HTTP (non sicura). In una configurazione predefinita, il protocollo di distribuzione video segue rigorosamente il protocollo di distribuzione della pagina Web in cui è stato incorporato. Tuttavia, è possibile imporre la distribuzione di video HTTPS senza tener conto del protocollo utilizzato dall&#39;incorporazione della pagina Web utilizzando l&#39;attributo di configurazione [VideoPlayer.ssl](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-ssl.md#reference-c28e1b700977493eadab5489458d7771). L’anteprima video in modalità Autore viene sempre trasmessa in modo protetto tramite HTTPS.

A seconda del metodo di pubblicazione del video Dynamic Media utilizzato in AEM, l&#39;attributo di configurazione `VideoPlayer.ssl` viene applicato in modo diverso, come illustrato di seguito:

* Se pubblicate un video Dynamic Media con un URL, aggiungete `VideoPlayer.ssl` all’URL. Ad esempio, per forzare la distribuzione sicura dei video, aggiungete `&VideoPlayer.ssl=on` alla fine del seguente esempio di URL visualizzatore:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/InteractiveVideoViewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Shoppable_Video_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&interactivedata=content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt&VideoPlayer.contenturl=https://adobedemo62-h.assetsadobe.com/is/content&VideoPlayer.ssl=on
   ```

   Vedere anche [Collegamento di URL all&#39;applicazione Web](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html)

* Se pubblicate un video Dynamic Media con codice da incorporare, aggiungete `VideoPlayer.ssl` all’elenco degli altri parametri di configurazione del visualizzatore nello snippet di codice da incorporare. Ad esempio, per imporre la distribuzione di video HTTPS, aggiungete `&VideoPlayer.ssl=on` come nell&#39;esempio seguente:

   ```
   <style type="text/css"> 
    #s7interactivevideo_div.s7interactivevideoviewer{ 
      width:100%;  
      height:auto; 
    } 
   </style> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <div id="s7interactivevideo_div"></div> 
   <script type="text/javascript"> 
    var s7interactivevideoviewer = new s7viewers.InteractiveVideoViewer({ 
     "containerId" : "s7interactivevideo_div", 
     "params" : {  
      "VideoPlayer.ssl" : "on", 
      "serverurl" : "https://adobedemo62-h.assetsadobe.com/is/image", 
      "contenturl" : "https://demos-pub.assetsadobe.com/",  
      "config" : "/etc/dam/presets/viewer/Shoppable_Video_light", 
      "config2": "/etc/dam/presets/analytics", 
      "videoserverurl": "https://gateway-na.assetsadobe.com/DMGateway/public/demoCo", 
      "interactivedata": "content/dam/_VTT/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4.svideo.vtt", 
      "VideoPlayer.contenturl": "https://adobedemo62-h.assetsadobe.com/is/content", 
      "asset" : "/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4" } 
    }) 
    /* // Example of interactive video event for quick view. 
      s7interactivevideoviewer.setHandlers({  
      "quickViewActivate": function(inData) { 
        var sku=inData.sku; //SKU for product ID 
       //To pass other parameter from the hotspot, you will need to add custom parameter during the hotspot setup as parameterName=value 
       loadQuickView(sku); //Replace this call with your quickview plugin 
       //Please refer to your quickviewer plugin for the quickview call 
       },  
   "initComplete":function() {  
       //--- Attach quickview popup to viewer container so popup will work in fullscreen mode --- 
       var popup = document.getElementById('quickview_div'); // get custom quick view container 
       popup.parentNode.removeChild(popup); // remove it from current DOM 
       var sdkContainerId = s7interactivevideoviewer.getComponent("container").getInnerContainerId(); // get viewer container component 
       var inner_container = document.getElementById(sdkContainerId);  
       inner_container.appendChild(popup); //Attach custom quick view container to viewer 
       }  
      }); 
    */ 
    s7interactivevideoviewer.init(); 
   </script>
   ```

   Vedere anche [Incorporazione del video in una pagina Web](https://docs.adobe.com/content/help/en/experience-manager-64/assets/dynamic/linking-urls-to-yourwebapplication.html).

