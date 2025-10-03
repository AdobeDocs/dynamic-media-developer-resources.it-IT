---
title: Consegna video HTTPS
description: Consegna video HTTPS
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 79f7e356-55d1-46e1-b85a-2e73633c9404
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---

# Consegna video HTTPS{#https-video-delivery}

<!-- >[!NOTE]
>
>HTTP Secure Video Delivery applies only to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Se il visualizzatore funziona nella configurazione come descritto all’inizio di questa sezione, la distribuzione di video pubblicati può avvenire sia in modalità HTTPS (sicura) che HTTP (non sicura). In una configurazione predefinita, il protocollo di consegna video segue rigorosamente il protocollo di consegna della pagina web in cui è incorporato. Tuttavia, è possibile forzare la consegna di video HTTPS indipendentemente dal protocollo utilizzato per incorporare la pagina Web utilizzando l&#39;attributo di configurazione [Video360Player.ssl](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-video360/r-html5-aem-video360-config-attrib/r-html5-aem-video360-config-attrib-video360player-ssl.md). L’anteprima video in modalità Creazione viene sempre distribuita in modo sicuro su HTTPS.

A seconda del metodo di pubblicazione del video Dynamic Media utilizzato in Adobe Experience Manager, l&#39;attributo di configurazione `Video360Player.ssl` viene applicato in modo diverso, come illustrato di seguito:

* Se pubblichi un video Dynamic Media con un URL, aggiungi `Video360Player.ssl` all&#39;URL.

<!-- For example, to force secure video delivery, you append `&Video360Player.ssl=on` to the end of the following viewer URL example: -->

<!--

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/Video360Viewer.html?asset=%2Fcontent%2Fdam%2Fmarketing%2Fshoppable-video%2Fadobe-axis-demo%2FAdobe_AXIS_V3_GRADED-HD.mp4&config=/etc/dam/presets/viewer/Video&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&posterimage=/content/dam/marketing/shoppable-video/adobe-axis-demo/Adobe_AXIS_V3_GRADED-HD.mp4&Video360Player.ssl=on
  ```

-->

Vedi anche [Collegamento di URL all&#39;applicazione Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=en#dynamic).

* Se pubblichi un video Dynamic Media con codice di incorporamento, aggiungi `Video360Player.ssl` all&#39;elenco degli altri parametri di configurazione del visualizzatore nel frammento di codice di incorporamento.

<!-- For example, to force HTTPS video delivery, you append `&Video360Player.ssl=on` as in the following example: -->

<!--

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

-->

Vedi anche [Incorporazione di un video in una pagina Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html#dynamic)
