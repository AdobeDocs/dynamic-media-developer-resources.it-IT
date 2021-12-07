---
title: Spazio dei nomi dell’SDK per visualizzatori
description: Spazio dei nomi dell’SDK per visualizzatori
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Spazio dei nomi dell’SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Di solito, la pagina web non deve interagire direttamente con i componenti SDK API; tutte le esigenze comuni sono coperte dall’API del visualizzatore stesso.

Tuttavia, alcuni casi d’uso avanzati richiedono che la pagina web faccia riferimento a un componente SDK interno utilizzando `getComponent()` API del visualizzatore e quindi usa tutta la flessibilità delle API dell’SDK stesso.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti SDK dipende dall’ambiente in cui opera il visualizzatore. Se il visualizzatore è in esecuzione in Adobe Experience Manager, il visualizzatore carica i componenti SDK in `s7viewers.s7sdk` spazio dei nomi. Allo stesso modo, il visualizzatore servito da Dynamic Media Classic carica l&#39;SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato dall’SDK all’interno del visualizzatore ha una delle seguenti caratteristiche: `s7viewers` o `s7classic` come prefisso. E, è diverso dalla pianura `s7sdk` namespace utilizzato nella Guida utente SDK o nella documentazione API SDK. Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando scrivi un codice applicativo personalizzato che comunica con i componenti del visualizzatore interni.

Ad esempio, se intendi ascoltare `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene servito dall&#39;Experience Manager, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`e il codice del listener di eventi è simile al seguente:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
