---
description: Il visualizzatore a comparsa supporta il tracciamento di Adobe Analytics.
seo-description: Il visualizzatore a comparsa supporta il tracciamento di Adobe Analytics.
seo-title: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
title: Supporto per il tracciamento di Adobe Analytics
topic: Dynamic media
uuid: ac5a2de9-6275-434f-ae09-a588f4a71aa6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore a comparsa supporta il tracciamento di Adobe Analytics.

## Tracciamento integrato {#section-ba994f079d0343c8ae48adffaa3195a3}

Il visualizzatore zoom in linea supporta il [!DNL Adobe Analytics] tracciamento out-of-the-box. Per abilitare il tracciamento, passate il nome corretto del predefinito della società come `config2` parametro.

Il visualizzatore invia inoltre un’unica richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per poter essere integrato con i sistemi di analisi di terze parti, è necessario ascoltare il callback del `trackEvent` visualizzatore ed elaborare l&#39; `eventInfo` argomento della funzione di callback come necessario. Il codice seguente è un esempio di tale funzione handler:

```
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
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
   <td colname="col2"> <p>una risorsa viene scambiata nel visualizzatore utilizzando l' <span class="codeph"> API setAsset() </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>il menu a comparsa viene attivato o il livello di zoom viene modificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">PAN (Panning)</span> </p> </td> 
   <td colname="col2"> <p> viene eseguito il panning di un’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">SWATCH (Campione)</span> </p> </td> 
   <td colname="col2"> <p> per modificare un’immagine, toccate o fate clic su un campione. </p> </td> 
  </tr> 
 </tbody> 
</table>

