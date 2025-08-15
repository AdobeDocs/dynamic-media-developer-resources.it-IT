---
title: Supporto per il tracciamento di Adobe Analytics
description: Il visualizzatore HTML5 Video360 supporta il tracciamento predefinito di Adobe Analytics.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User,Data Engineer,Data Architect
exl-id: 74a69d01-fa58-4d36-8598-992baf6ae11d
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore HTML5 Video360 supporta il tracciamento predefinito di Adobe Analytics.

Per abilitare il tracciamento, passa il nome del predefinito della società corretto come parametro `config2`.

Per impostazione predefinita, il visualizzatore invia una singola richiesta HTTP di tracciamento al server immagini configurato con le informazioni sul tipo e sulla versione del visualizzatore.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per l&#39;integrazione con sistemi di analisi di terze parti, è necessario ascoltare il callback del visualizzatore `trackEvent` ed elaborare l&#39;argomento `eventInfo` della funzione di callback in base alle esigenze. Il codice che segue è un esempio di tale funzione di gestore:

```javascript {.line-numbers}
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

Il visualizzatore tiene traccia dei seguenti eventi utente di SDK:

<table id="table_5D090E6614974D968E1A93B5727D859C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento utente SDK </p> </th> 
   <th colname="col2" class="entry"> <p>Inviato... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CARICAMENTO </span> </p> </td> 
   <td colname="col2"> <p>quando il visualizzatore viene caricato per primo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SCAMBIO </span> </p> </td> 
   <td colname="col2"> <p>quando una risorsa viene scambiata nel visualizzatore utilizzando l'API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RIPRODUCI </span> </p> </td> 
   <td colname="col2"> <p>all’avvio della riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PAUSA </span> </p> </td> 
   <td colname="col2"> <p>quando la riproduzione viene messa in pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> INTERROMPI </span> </p> </td> 
   <td colname="col2"> <p>quando la riproduzione viene interrotta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MILESTONE </span> </p> </td> 
   <td colname="col2"> <p>quando la riproduzione raggiunge uno dei seguenti target cardine: 0%, 25%, 50%, 75% o 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>
