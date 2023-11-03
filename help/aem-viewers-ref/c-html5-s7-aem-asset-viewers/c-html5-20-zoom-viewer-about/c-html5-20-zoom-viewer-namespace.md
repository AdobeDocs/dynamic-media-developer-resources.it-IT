---
title: Spazio dei nomi SDK per visualizzatori
description: Spazio dei nomi SDK per visualizzatori
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ad68dd09-d8df-4fc8-952a-ef82d9662de9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Spazio dei nomi SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Di solito, la pagina web non deve interagire direttamente con l’API dei componenti SDK; tutte le esigenze comuni sono coperte nell’API del visualizzatore stessa.

Tuttavia, alcuni casi d’uso avanzati richiedono che la pagina web faccia riferimento a un componente SDK interno utilizzando `getComponent()` e quindi utilizzare tutta la flessibilità delle API dell’SDK stesso.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti SDK dipende dall’ambiente in cui opera il visualizzatore. Se il visualizzatore è in esecuzione in Adobe Experience Manager, carica i componenti SDK in `s7viewers.s7sdk` spazio dei nomi. Allo stesso modo, il visualizzatore fornito da Dynamic Media Classic carica l’SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato dall’SDK nel visualizzatore ha `s7viewers` o `s7classic` come prefisso. Ed è diverso dal semplice `s7sdk` spazio dei nomi utilizzato nella Guida utente dell’SDK o nella documentazione API dell’SDK. Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando scrivi codice personalizzato dell’applicazione che comunica con i componenti interni del visualizzatore.

Ad esempio, se intendi ascoltare `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene gestito da Experience Manager, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`e il codice del listener di eventi è simile al seguente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
