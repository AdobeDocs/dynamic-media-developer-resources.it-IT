---
title: Supporto per il tracciamento di Adobe Analytics
description: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 4%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Per impostazione predefinita, il visualizzatore invia una singola richiesta HTTP di tracciamento al server immagini configurato con le informazioni sul tipo e sulla versione del visualizzatore.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per l’integrazione con sistemi di analisi di terze parti, è necessario ascoltare `trackEvent` callback del visualizzatore ed elaborare `eventInfo` della funzione di callback, se necessario. Il codice che segue è un esempio di tale funzione di gestore:

```javascript {.line-numbers}
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
    break; 
   case "INTERACTIVE_SWATCH": 
    //custom event processing code which handles user clicks on interactive swatches 
    break; 
   //additional cases for other events 
} 
} 
} 
});
```

Il visualizzatore tiene traccia dei seguenti eventi utente SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento utente SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Inviato... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">LOAD (Caricamento)</span> </p> </td> 
   <td colname="col2"> <p>quando il visualizzatore viene caricato per primo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">SWAP (Scambio)</span> </p> </td> 
   <td colname="col2"> <p>quando una risorsa viene scambiata nel visualizzatore utilizzando <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PLAY (Riproduzione)</span> </p> </td> 
   <td colname="col2"> <p>all’avvio della riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAUSE (Pausa)</span> </p> </td> 
   <td colname="col2"> <p>quando la riproduzione viene messa in pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">STOP (Interruzione)</span> </p> </td> 
   <td colname="col2"> <p>quando la riproduzione viene interrotta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">MILESTONE (Pietra miliare)</span> </p> </td> 
   <td colname="col2"> <p>quando la riproduzione raggiunge uno dei seguenti target cardine: 0%, 25%, 50%, 75% o 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAMPIONE_INTERATTIVO </span> </p> </td> 
   <td colname="col2"> <p>ogni volta che l’utente fa clic su un campione interattivo. </p> </td> 
  </tr> 
 </tbody> 
</table>
