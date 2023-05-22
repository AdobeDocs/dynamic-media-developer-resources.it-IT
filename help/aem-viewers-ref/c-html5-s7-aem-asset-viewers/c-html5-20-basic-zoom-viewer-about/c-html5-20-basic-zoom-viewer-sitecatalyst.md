---
title: Supporto per il tracciamento di Adobe Analytics
description: Il visualizzatore zoom di base supporta il tracciamento Adobe Analytics preconfigurato.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User,Data Engineer,Data Architect
exl-id: 5b9d871d-9f37-4908-900e-3f0ecc98bc0c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore zoom di base supporta il tracciamento Adobe Analytics preconfigurato.

## Tracciamento predefinito {#section-ba994f079d0343c8ae48adffaa3195a3}

Il visualizzatore zoom di base supporta [!DNL Adobe Analytics] tracciamento preconfigurato. Per abilitare il tracciamento, passa il nome del predefinito aziendale corretto come `config2` parametro.

Il visualizzatore invia anche una singola richiesta HTTP di tracciamento al server immagini configurato con le informazioni sul tipo e sulla versione del visualizzatore.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per l’integrazione con sistemi di analisi di terze parti, è necessario ascoltare `trackEvent` callback del visualizzatore ed elaborare `eventInfo` della funzione di callback, se necessario. Il codice che segue è un esempio di tale funzione di gestore:

```javascript {.line-numbers}
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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
   <th colname="col2" class="entry"> <p>Inviato quando... </p> </th> 
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
   <td colname="col2"> <p> un'immagine è ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAN (Panning)</span> </p> </td> 
   <td colname="col2"> <p>un'immagine è sottoposta a panning. </p> </td> 
  </tr> 
 </tbody> 
</table>
