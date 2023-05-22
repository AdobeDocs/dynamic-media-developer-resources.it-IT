---
title: Consegna video HTTPS
description: Consegna video HTTPS
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Consegna video HTTPS{#https-video-delivery}

<!-- >[!NOTE]
>
>HTTP Secure Video Delivery applies only to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Se il visualizzatore funziona nella configurazione come descritto all’inizio di questa sezione, la distribuzione di video pubblicati può avvenire sia in modalità HTTPS (sicura) che HTTP (non sicura). In una configurazione predefinita, il protocollo di consegna video segue rigorosamente il protocollo di consegna della pagina web in cui è incorporato. Tuttavia, è possibile forzare la consegna di video HTTPS indipendentemente dal protocollo utilizzato per incorporare la pagina web utilizzando [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md) attributo di configurazione. L’anteprima video in modalità Creazione viene sempre distribuita in modo sicuro su HTTPS.

A seconda del metodo di pubblicazione dei video Dynamic Media utilizzato in Adobe Experience Manager, il `Video360Player.ssl` l’attributo di configurazione viene applicato in modo diverso, come dimostrato di seguito:

* Se pubblichi un video Dynamic Media con un URL, aggiungi `Video360Player.ssl` all&#39;URL. Ad esempio, per forzare la distribuzione sicura dei video, aggiungi `&Video360Player.ssl=on` alla fine del seguente esempio di URL visualizzatore:

   ```
   https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
   ```

   Vedi anche [Collegamento di URL all’applicazione web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Se pubblichi un video Dynamic Media con codice da incorporare, aggiungi `Video360Player.ssl` nell’elenco degli altri parametri di configurazione del visualizzatore nello snippet di codice da incorporare. Ad esempio, per forzare la consegna di video HTTPS, aggiungi `&Video360Player.ssl=on` come nell’esempio seguente:

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

   Vedi anche [Incorporare il video in una pagina web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)
