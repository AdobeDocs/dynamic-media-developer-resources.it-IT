---
title: Spazio dei nomi dell’SDK per visualizzatori
description: Spazio dei nomi dell’SDK per visualizzatori
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b61a17-f9ae-4e71-bd78-276674193044
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Spazio dei nomi dell’SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Di solito, la pagina web non deve interagire direttamente con i componenti SDK API; tutte le esigenze comuni sono coperte dall’API del visualizzatore stesso.

Tuttavia, alcuni casi d’uso avanzati richiedono che la pagina web faccia riferimento a un componente SDK interno utilizzando `getComponent()` API del visualizzatore e quindi usa tutta la flessibilità delle API dell’SDK stesso.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti SDK dipende dall’ambiente in cui opera il visualizzatore. Se il visualizzatore è in esecuzione in Adobe Experience Manager, il visualizzatore carica i componenti SDK in `s7viewers.s7sdk` spazio dei nomi. Allo stesso modo, il visualizzatore servito da Dynamic Media Classic carica l&#39;SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato dall’SDK all’interno del visualizzatore ha una delle seguenti caratteristiche: `s7viewers` o `s7classic` come prefisso. E, è diverso dalla pianura `s7sdk` namespace utilizzato nella Guida utente SDK o nella documentazione API SDK.

Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando scrivi un codice applicativo personalizzato che comunica con i componenti del visualizzatore interni.

Ad esempio, se intendi ascoltare `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene servito dall&#39;Experience Manager, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`e il codice del listener di eventi è simile al seguente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
