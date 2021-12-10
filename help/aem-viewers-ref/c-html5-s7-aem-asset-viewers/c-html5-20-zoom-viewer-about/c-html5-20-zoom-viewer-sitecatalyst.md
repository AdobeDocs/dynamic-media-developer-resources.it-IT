---
title: Supporto per il tracciamento di Adobe Analytics
description: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User,Data Engineer,Data Architect
exl-id: 5f927a4b-b9c8-4750-9d1c-c252d87fd236
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

## Tracciamento preconfigurato {#section-ba994f079d0343c8ae48adffaa3195a3}

Il visualizzatore video supporta [!DNL Adobe Analytics] tracciamento preconfigurato. Per abilitare il tracciamento, passa il nome corretto del predefinito aziendale come `config2` parametro .

Il visualizzatore invia inoltre una singola richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per integrare con sistemi di analisi di terze parti, è necessario ascoltare `trackEvent` callback ed elaborazione del visualizzatore `eventInfo` argomento della funzione di callback, se necessario. Il codice seguente è un esempio di tale funzione di gestione:

```
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "trackEvent":function(objID, compClass, instName, timeStamp, eventInfo) { 
  //identify event type 
  var eventType = eventInfo.split(",")[0]; 
  switch (eventType) { 
   case "LOAD": 
    //custom event processing code 
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
   <th colname="col2" class="entry"> <p>Inviato quando.. </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">LOAD (Caricamento)</span> </p> </td> 
   <td colname="col2"> <p>il visualizzatore viene caricato per primo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">SWAP (Scambio)</span> </p> </td> 
   <td colname="col2"> <p>una risorsa viene scambiata nel visualizzatore utilizzando <span class="codeph"> setAsset() </span> API. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> un’immagine viene ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAN (Panning)</span> </p> </td> 
   <td colname="col2"> <p>un'immagine viene pannerizzata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">SWATCH (Campione)</span> </p> </td> 
   <td colname="col2"> <p> per modificare un’immagine, toccate o fate clic su un campione. </p> </td> 
  </tr> 
 </tbody> 
</table>
