---
description: Il visualizzatore video supporta il tracciamento out-of-the-box di Adobe Analytics.
seo-description: Il visualizzatore video supporta il tracciamento out-of-the-box di Adobe Analytics.
seo-title: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
title: Supporto per il tracciamento di Adobe Analytics
topic: Dynamic media
uuid: c53b3d3b-42e5-4c87-8a1e-87c73eb32341
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore video supporta il tracciamento out-of-the-box di Adobe Analytics.

## Tracciamento integrato {#section-3b101fe30be943c1b679fd5c273569ca}

Il visualizzatore video supporta il tracciamento out-of-the-box di Adobe Analytics.

Per abilitare il tracciamento, passate il nome corretto del predefinito della società come `config2` parametro.

Il visualizzatore invia inoltre un’unica richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-ab10bd7caf184721a366cf3953071934}

Per poter essere integrato con i sistemi di analisi di terze parti, è necessario ascoltare il callback del `trackEvent` visualizzatore e l&#39;argomento di elaborazione `eventInfo` della funzione di callback, a seconda delle necessità. Il codice seguente è un esempio di tale funzione handler:

```
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
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
   <td colname="col2"> <p>una risorsa viene scambiata nel visualizzatore utilizzando l' <span class="codeph"> API setAsset() </span> . </p> </td> 
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
   <td colname="col2"> <p>la riproduzione raggiunge uno dei seguenti mosaici: 0%, 25%, 50%, 75% e 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

