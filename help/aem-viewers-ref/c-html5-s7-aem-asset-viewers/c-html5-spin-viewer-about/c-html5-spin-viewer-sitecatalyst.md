---
description: Il visualizzatore per set 360 gradi supporta  tracciamento Adobe Analytics.
seo-description: Il visualizzatore per set 360 gradi supporta  tracciamento Adobe Analytics.
seo-title: Supporto per  tracciamento Adobe Analytics
solution: Experience Manager
title: Supporto per  tracciamento Adobe Analytics
topic: Dynamic media
uuid: 337671f0-22e8-4e3e-a0a9-ce49d271ea56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---


# Supporto per  tracciamento Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore per set 360 gradi supporta  tracciamento Adobe Analytics.

## Tracciamento out-of-the-box {#section-d06145cfa2b9491bb485b599368d466e}

Il visualizzatore 360 gradi supporta  tracciamento Adobe Analytics out-of-the-box.

Per abilitare il tracciamento, passate il nome corretto del predefinito della società come parametro `config2`.

Il visualizzatore invia inoltre un’unica richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-47512156a1d64b338b50cfa39c84f4aa}

Per poter essere integrato con i sistemi di analisi di terze parti, è necessario ascoltare il callback del visualizzatore `trackEvent` ed elaborare l&#39;argomento `eventInfo` della funzione di callback, se necessario. Il codice seguente è un esempio di tale funzione handler:

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
   <td colname="col2"> <p>una risorsa viene scambiata nel visualizzatore utilizzando l'API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> viene applicato lo zoom a un’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAN (Panning)</span> </p> </td> 
   <td colname="col2"> <p>viene eseguito il panning di un’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">SPIN (Set a 360 gradi)</span> </p> </td> 
   <td colname="col2"> <p> viene eseguito un giro. </p> </td> 
  </tr> 
 </tbody> 
</table>

