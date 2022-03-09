---
description: Il visualizzatore di ricerca per eCatalog supporta il tracciamento di Adobe Analytics.
solution: Experience Manager
title: Supporto per il tracciamento di Adobe Analytics
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User,Data Engineer,Data Architect
exl-id: b35e52f5-fa08-4945-aa52-9fdf41a6081a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 4%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore di ricerca per eCatalog supporta il tracciamento di Adobe Analytics.

## Tracciamento preconfigurato {#section-ba994f079d0343c8ae48adffaa3195a3}

Il visualizzatore di ricerca per eCatalog supporta [!DNL Adobe Analytics] tracciamento preconfigurato. Per abilitare il tracciamento, passa il nome corretto del predefinito aziendale come `config2` parametro .

Il visualizzatore invia inoltre una singola richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per integrare con sistemi di analisi di terze parti è necessario ascoltare `trackEvent` callback ed elaborazione del visualizzatore `eventInfo` argomento della funzione di callback, se necessario. Il codice seguente è un esempio di tale funzione di gestione:

```javascript {.line-numbers}
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p> un’immagine viene ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAN (Panning)</span> </p> </td> 
   <td colname="col2"> <p>un'immagine viene pannerizzata. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">SWATCH (Campione)</span> </p> </td> 
   <td colname="col2"> <p> per modificare un’immagine, toccate o fate clic su un campione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAGE (Pagina)</span> </p> </td> 
   <td colname="col2"> <p> nella vista principale viene modificato un fotogramma corrente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">ITEM (Elemento)</span> </p> </td> 
   <td colname="col2"> <p>viene attivato un pop-up del pannello informazioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>un utente passa a una pagina diversa facendo clic sulla mappa immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>
