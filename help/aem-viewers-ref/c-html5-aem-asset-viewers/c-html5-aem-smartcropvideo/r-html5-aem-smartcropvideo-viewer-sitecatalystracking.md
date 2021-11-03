---
title: Supporto per il tracciamento di Adobe Analytics
description: Il visualizzatore video Smart Crop supporta il tracciamento predefinito di Adobe Analytics.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User,Data Engineer,Data Architect
exl-id: 2cc7087d-ed02-4560-b9ce-533af2b11a24
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore video Smart Crop supporta il tracciamento predefinito di Adobe Analytics.

## Tracciamento preconfigurato {#section-3b101fe30be943c1b679fd5c273569ca}

Il visualizzatore video Smart Crop supporta il tracciamento predefinito di Adobe Analytics.

Per abilitare il tracciamento, passa il nome corretto del predefinito aziendale come `config2` parametro .

Il visualizzatore invia inoltre una singola richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-ab10bd7caf184721a366cf3953071934}

Per integrare con sistemi di analisi di terze parti, è necessario ascoltare `trackEvent` callback ed elaborazione del visualizzatore `eventInfo` argomento della funzione di callback, se necessario. Il codice seguente è un esempio di tale funzione di gestione:

```
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
   <td colname="col1"> <p> <span class="codeph">PLAY (Riproduzione)</span> </p> </td> 
   <td colname="col2"> <p>la riproduzione viene avviata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAUSE (Pausa)</span> </p> </td> 
   <td colname="col2"> <p>la riproduzione viene messa in pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">STOP (Interruzione)</span> </p> </td> 
   <td colname="col2"> <p>la riproduzione viene interrotta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">MILESTONE (Pietra miliare)</span> </p> </td> 
   <td colname="col2"> <p>la riproduzione raggiunge una delle seguenti pietre miliari: 0%, 25%, 50%, 75% e 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>
