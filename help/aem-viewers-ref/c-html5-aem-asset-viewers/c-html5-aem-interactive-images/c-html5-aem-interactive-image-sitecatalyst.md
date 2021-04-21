---
description: Supporto per il tracciamento delle analisi
solution: Experience Manager
title: Supporto per il tracciamento delle analisi
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner,Data Engineer,Data Architect
exl-id: 17e8937f-e328-46a4-b7d9-1fd39ab2e8bd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---

# Supporto per il tracciamento delle analisi{#support-for-analytics-tracking}

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per impostazione predefinita, il visualizzatore invia una singola richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

Per integrarsi con sistemi di analisi di terze parti, è necessario ascoltare il callback del visualizzatore `trackEvent` ed elaborare l&#39;argomento `eventInfo` della funzione di callback, a seconda delle necessità. Il codice seguente è un esempio di tale funzione di gestione:

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
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
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>l’utente attiva il punto attivo. </p> </td> 
  </tr> 
 </tbody> 
</table>
