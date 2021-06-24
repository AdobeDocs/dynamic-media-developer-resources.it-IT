---
description: Il visualizzatore a 360 gradi supporta il tracciamento di Adobe Analytics.
solution: Experience Manager
title: Supporto per il tracciamento di Adobe Analytics
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Developer,Business Practitioner,Data Engineer,Data Architect
exl-id: 30762700-6d69-4299-9492-57893232abe1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore a 360 gradi supporta il tracciamento di Adobe Analytics.

## Tracciamento preconfigurato {#section-d06145cfa2b9491bb485b599368d466e}

Il visualizzatore a 360 gradi supporta il tracciamento predefinito di Adobe Analytics.

Per abilitare il tracciamento, passa il nome corretto del predefinito aziendale come parametro `config2` .

Il visualizzatore invia inoltre una singola richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-47512156a1d64b338b50cfa39c84f4aa}

Per integrarsi con sistemi di analisi di terze parti, è necessario ascoltare il callback del visualizzatore `trackEvent` ed elaborare l&#39;argomento `eventInfo` della funzione di callback, a seconda delle necessità. Il codice seguente è un esempio di tale funzione di gestione:

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
   <td colname="col2"> <p>una risorsa viene scambiata nel visualizzatore utilizzando l’ API <span class="codeph"> setAsset() </span> . </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph">SPIN (Set a 360 gradi)</span> </p> </td> 
   <td colname="col2"> <p> viene eseguita una rotazione. </p> </td> 
  </tr> 
 </tbody> 
</table>
