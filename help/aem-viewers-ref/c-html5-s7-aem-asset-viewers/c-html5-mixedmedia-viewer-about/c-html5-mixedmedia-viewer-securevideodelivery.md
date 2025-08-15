---
title: Consegna video HTTPS
description: Consegna video HTTPS
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f9651405-ebc6-4b1f-8fb6-031d0b295083
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Consegna video HTTPS{#https-video-delivery}

<!-- >[!NOTE]
>
>Secure Video Delivery only applies to AEM 6.2 with the installation of [Feature Pack-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) and to AEM 6.1 with installation of [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011). -->

Se il visualizzatore funziona nella configurazione come descritto all’inizio di questa sezione, la distribuzione di video pubblicati può avvenire sia in modalità HTTPS (sicura) che HTTP (non sicura). In una configurazione predefinita, il protocollo di consegna video segue rigorosamente il protocollo di consegna della pagina web in cui è incorporato. Tuttavia, è possibile forzare la consegna di video HTTPS indipendentemente dal protocollo utilizzato per incorporare la pagina Web utilizzando l&#39;attributo di configurazione [VideoPlayer.ssl](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-ssl.md#reference-df0a29aa8a584cebaaa1c7bb6fab362e). L’anteprima video in modalità Creazione viene sempre distribuita in modo sicuro su HTTPS.

A seconda del metodo di pubblicazione del video Dynamic Media utilizzato in Adobe Experience Manager, l&#39;attributo di configurazione `VideoPlayer.ssl` viene applicato in modo diverso, come illustrato di seguito:

* Se pubblichi un video Dynamic Media con un URL, aggiungi `VideoPlayer.ssl` all&#39;URL. Ad esempio, per forzare la consegna sicura dei video, aggiungi `&VideoPlayer.ssl=on` alla fine del seguente esempio di URL visualizzatore:

  ```
  https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/MixedMediaViewer.html?asset=%2Fcontent%2Fdam%2FGeometrixx-Outdoors-New-Launch%2Fbackpack%2Fbackpack_mixed_media&config=/etc/dam/presets/viewer/MixedMedia_light&serverUrl=https%3A%2F%2Fadobedemo62-h.assetsadobe.com%2Fis%2Fimage%2F&contenturl=%2F&config2=/etc/dam/presets/analytics&videoserverurl=https://gateway-na.assetsadobe.com/DMGateway/public/demoCo&VideoPlayer.ssl=on
  ```

  Vedi anche [(Collegamento degli URL all&#39;applicazione Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=it#dynamic).

* Se pubblichi un video Dynamic Media con codice di incorporamento, aggiungi `VideoPlayer.ssl` all&#39;elenco degli altri parametri di configurazione del visualizzatore nel frammento di codice di incorporamento. Ad esempio, per forzare la consegna di video HTTPS, aggiungi `&VideoPlayer.ssl=on` come nell&#39;esempio seguente:

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

  Vedere anche [(Incorporazione del video in una pagina Web](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/linking-urls-to-yourwebapplication.html?lang=it#dynamic).
