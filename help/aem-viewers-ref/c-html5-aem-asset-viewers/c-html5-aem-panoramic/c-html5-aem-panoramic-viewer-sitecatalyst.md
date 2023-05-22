---
title: Supporto per il tracciamento di Adobe Analytics
description: Supporto per il tracciamento di Adobe Analytics
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User,Data Engineer,Data Architect
exl-id: fb58a388-e4da-475d-b726-d5a32e99cce0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 1%

---

# Supporto per il tracciamento di Adobe Analytics{#support-for-adobe-analytics-tracking}

Per impostazione predefinita, il visualizzatore invia una singola richiesta HTTP di tracciamento al server immagini configurato con informazioni sul tipo e sulla versione del visualizzatore.

## Tracciamento personalizzato {#section-cda48fc9730142d0bb3326bac7df3271}

Per integrarsi con un sistema di analisi di terze parti è necessario ascoltare `trackEvent` callback ed elaborazione del visualizzatore `eventInfo` della funzione di callback, se necessario. Il codice che segue è un esempio di tale funzione di gestore:

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
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
   <th colname="col2" class="entry"> <p>Inviato... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">LOAD (Caricamento)</span> </p> </td> 
   <td colname="col2"> <p>quando il visualizzatore viene caricato per primo. </p> </td> 
  </tr> 
 </tbody> 
</table>
