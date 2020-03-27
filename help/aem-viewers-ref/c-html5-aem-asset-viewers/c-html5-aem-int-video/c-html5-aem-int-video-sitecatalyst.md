---
description: Il visualizzatore HTML5 Video360 supporta il tracciamento out-of-the-box di Adobe Analytics.
seo-description: Il visualizzatore HTML5 Video360 supporta il tracciamento out-of-the-box di Adobe Analytics.
seo-title: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
title: Supporto per il tracciamento di Adobe Analytics
topic: Dynamic media
uuid: b5ab903b-3365-45e3-9542-c290c6c42670
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore HTML5 Video360 supporta il tracciamento out-of-the-box di Adobe Analytics.

Per abilitare il tracciamento, passate il nome corretto del predefinito della società come `config2` parametro.

Per impostazione predefinita, il visualizzatore invia un’unica richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per poter essere integrato con i sistemi di analisi di terze parti, è necessario ascoltare il callback del `trackEvent` visualizzatore ed elaborare l&#39; `eventInfo` argomento della funzione di callback come necessario. Il codice seguente è un esempio di tale funzione handler:

```
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
   <td colname="col2"> <p>quando una risorsa viene scambiata nel visualizzatore tramite l’ <span class="codeph"> API setAsset() </span> . </p> </td> 
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
   <td colname="col2"> <p>quando la riproduzione raggiunge uno dei seguenti traguardi: 0%, 25%, 50%, 75% o 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

