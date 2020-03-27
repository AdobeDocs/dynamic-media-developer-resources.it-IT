---
description: Il visualizzatore di eCatalog supporta il tracciamento di Adobe Analytics.
seo-description: Il visualizzatore di eCatalog supporta il tracciamento di Adobe Analytics.
seo-title: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
title: Supporto per il tracciamento di Adobe Analytics
topic: Dynamic media
uuid: a96b6655-4a11-490c-8f66-3633f0ae0fee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore di eCatalog supporta il tracciamento di Adobe Analytics.

## Tracciamento integrato {#section-ba994f079d0343c8ae48adffaa3195a3}

Il visualizzatore per eCatalog supporta il [!DNL Adobe Analytics] tracciamento out-of-the-box. Per abilitare il tracciamento, passate il nome corretto del predefinito della società come `config2` parametro.

Il visualizzatore invia inoltre un’unica richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per poter essere integrato con i sistemi di analisi di terze parti, è necessario ascoltare il callback del `trackEvent` visualizzatore ed elaborare l&#39; `eventInfo` argomento della funzione di callback come necessario. Il codice seguente è un esempio di tale funzione handler:

```
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
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
   <td colname="col2"> <p>una risorsa viene scambiata nel visualizzatore tramite l’ <span class="codeph"> API setAsset() </span> . </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph">SWATCH (Campione)</span> </p> </td> 
   <td colname="col2"> <p> per modificare un’immagine, toccate o fate clic su un campione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAGE (Pagina)</span> </p> </td> 
   <td colname="col2"> <p> nella vista principale viene modificato un fotogramma corrente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">ITEM (Elemento)</span> </p> </td> 
   <td colname="col2"> <p>viene attivata una finestra a comparsa del pannello Info. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> HREF </span> </p> </td> 
   <td colname="col2"> <p>un utente passa a un’altra pagina facendo clic sulla mappa immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

