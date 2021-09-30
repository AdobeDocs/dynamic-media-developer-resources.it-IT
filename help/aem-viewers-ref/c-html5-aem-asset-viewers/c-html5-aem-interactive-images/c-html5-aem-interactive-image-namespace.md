---
title: Spazio dei nomi dell’SDK per visualizzatori
description: Spazio dei nomi dell’SDK per visualizzatori
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8e37bb60-c875-48d6-8c86-93aba7f50f74
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Spazio dei nomi dell’SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Di solito, la pagina web non deve interagire direttamente con l’API dei componenti SDK; tutte le esigenze comuni sono coperte dall’API del visualizzatore stesso.

Tuttavia, alcuni casi d’uso avanzati richiedono che la pagina web faccia riferimento a un componente SDK interno utilizzando l’ API del visualizzatore `getComponent()` e quindi che utilizzi tutta la flessibilità delle API dell’SDK stesso.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti SDK dipende dall’ambiente in cui opera il visualizzatore. Se il visualizzatore è in esecuzione in Adobe Experience Manager, il visualizzatore carica i componenti SDK nello spazio dei nomi `s7viewers.s7sdk` . E il visualizzatore servito da Dynamic Media Classic carica l&#39;SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato dall’SDK all’interno del visualizzatore ha `s7viewers` o `s7classic` come prefisso. Inoltre, è diverso dallo spazio dei nomi semplice `s7sdk` utilizzato nella Guida utente SDK o nella documentazione API SDK.

Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando scrivi un codice di applicazione personalizzato che comunica con i componenti del visualizzatore interni.

Ad esempio, se prevedi di ascoltare l’evento `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene servito dall’Experience Manager, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e il codice del listener di eventi è simile al seguente:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
