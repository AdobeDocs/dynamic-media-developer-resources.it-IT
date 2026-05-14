---
title: Supporto per il tracciamento di Adobe Analytics
description: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 5f927a4b-b9c8-4750-9d1c-c252d87fd236
TQID: 'https://experienceleague.adobe.com/4XIzFFsX43NZBy4uB5WRZeIs92EWpbT8U2BsnTsmlDU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 0%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

## Tracciamento predefinito {#section-ba994f079d0343c8ae48adffaa3195a3}

Il Visualizzatore video supporta il tracciamento predefinito di [!DNL Adobe Analytics]. Per abilitare il tracciamento, passa il nome del predefinito della società corretto come parametro `config2`.

Il visualizzatore invia anche una singola richiesta HTTP di tracciamento al server immagini configurato con le informazioni sul tipo e sulla versione del visualizzatore.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per l&#39;integrazione con sistemi di analisi di terze parti, è necessario ascoltare il callback del visualizzatore `trackEvent` ed elaborare l&#39;argomento `eventInfo` della funzione di callback in base alle esigenze. Il codice che segue è un esempio di tale funzione di gestore:

```javascript {.line-numbers}
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

Il visualizzatore tiene traccia dei seguenti eventi utente di SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento utente SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Inviato quando... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CARICAMENTO </span> </p> </td> 
   <td colname="col2"> <p>il visualizzatore viene caricato per primo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SCAMBIO </span> </p> </td> 
   <td colname="col2"> <p>una risorsa viene scambiata nel visualizzatore utilizzando l'API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> un'immagine è ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PANORAMICA </span> </p> </td> 
   <td colname="col2"> <p>un'immagine è sottoposta a panning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAMPIONE </span> </p> </td> 
   <td colname="col2"> <p> per modificare un’immagine tocca o fai clic su un campione. </p> </td> 
  </tr> 
 </tbody> 
</table>
