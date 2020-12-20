---
description: Il visualizzatore per file multimediali diversi supporta  tracciamento Adobe Analytics out-of-the-box.
seo-description: Il visualizzatore per file multimediali diversi supporta  tracciamento Adobe Analytics out-of-the-box.
seo-title: Supporto per  tracciamento Adobe Analytics
solution: Experience Manager
title: Supporto per  tracciamento Adobe Analytics
topic: Dynamic media
uuid: ad4dfed6-121f-4adb-bbdb-db6e6ee5672d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 5%

---


# Supporto per  tracciamento Adobe Analytics{#support-for-adobe-analytics-tracking}

Il visualizzatore per file multimediali diversi supporta  tracciamento Adobe Analytics out-of-the-box.

## Tracciamento out-of-the-box {#section-ba994f079d0343c8ae48adffaa3195a3}

Il visualizzatore per file multimediali diversi supporta il monitoraggio out-of-the-box di [!DNL Adobe Analytics]. Per abilitare il tracciamento, passate il nome corretto del predefinito della società come parametro `config2`.

Il visualizzatore invia inoltre un’unica richiesta HTTP di tracciamento al server immagini configurato con il tipo di visualizzatore e le informazioni sulla versione.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per poter essere integrato con i sistemi di analisi di terze parti, è necessario ascoltare il callback del visualizzatore `trackEvent` ed elaborare l&#39;argomento `eventInfo` della funzione di callback come necessario. Il codice seguente è un esempio di tale funzione handler:

```
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
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
   <td colname="col2"> <p>una risorsa viene scambiata nel visualizzatore utilizzando l'API <span class="codeph"> setAsset() </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZOOM </span> </p> </td> 
   <td colname="col2"> <p>viene applicato lo zoom a un’immagine. </p> </td> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph">SPIN (Set a 360 gradi)</span> </p> </td> 
   <td colname="col2"> <p>viene eseguito il spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

