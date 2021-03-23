---
description: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
title: Supporto per il tracciamento di Adobe Analytics
uuid: a7de5549-2a9d-4153-be5e-72705ced85ac
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Sviluppatore,Business Practitioner,Data Engineer,Data Architect
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 1%

---


# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per impostazione predefinita, il visualizzatore invia una singola richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

Per integrarsi con sistemi di analisi di terze parti, è necessario ascoltare il callback del visualizzatore `trackEvent` ed elaborare l&#39;argomento `eventInfo` della funzione di callback, a seconda delle necessità. Il codice seguente è un esempio di tale funzione di gestione:

```
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
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
   <td colname="col1"> <p> <span class="codeph"> BANNER  </span> </p> </td> 
   <td colname="col2"> <p>l’immagine del banner carosello viene modificata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>l’utente attiva il punto attivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

