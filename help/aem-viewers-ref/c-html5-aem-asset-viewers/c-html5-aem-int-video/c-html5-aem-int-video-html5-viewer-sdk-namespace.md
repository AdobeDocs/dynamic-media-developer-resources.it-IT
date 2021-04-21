---
description: Spazio dei nomi dell’SDK per visualizzatori
solution: Experience Manager
title: Spazio dei nomi dell’SDK per visualizzatori
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 4a4d821e-9351-4efa-8849-968e746911f3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Spazio dei nomi SDK del visualizzatore{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Nella maggior parte dei casi, la pagina web non deve interagire direttamente con l’API dei componenti SDK; tutte le esigenze comuni sono coperte dall’API del visualizzatore stesso.

Tuttavia, alcuni casi d’uso avanzati richiedono che la pagina web ottenga un riferimento a un componente SDK interno utilizzando l’ API visualizzatore `getComponent()` e quindi utilizzi tutta la flessibilità delle API dell’SDK stesso.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti SDK dipende dall’ambiente in cui opera il visualizzatore. Se il visualizzatore è in esecuzione in AEM (Adobe Experience Manager), il visualizzatore carica i componenti SDK nello spazio dei nomi `s7viewers.s7sdk` . Allo stesso modo, il visualizzatore servito da Dynamic Media Classic carica l&#39;SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato dall’SDK all’interno del visualizzatore ha `s7viewers` o `s7classic` come prefisso. Inoltre, è diverso dallo spazio dei nomi semplice `s7sdk` utilizzato nella Guida utente SDK o nella documentazione API SDK.

Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando scrivi un codice di applicazione personalizzato che comunica con i componenti del visualizzatore interni.

Ad esempio, se prevedi di ascoltare l’evento `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene servito da AEM, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e il codice del listener di eventi è simile al seguente:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
