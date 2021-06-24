---
description: Spazio dei nomi dell’SDK per visualizzatori
solution: Experience Manager
title: Spazio dei nomi dell’SDK per visualizzatori
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,Business Practitioner
exl-id: 1712f08c-70e6-483e-a4e5-614448f35374
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Spazio dei nomi dell’SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Nella maggior parte dei casi, la pagina web non deve interagire direttamente con l’API dei componenti SDK; tutte le esigenze comuni sono coperte dall’API del visualizzatore stesso.

Tuttavia, alcuni casi d’uso avanzati richiedono che la pagina web ottenga un riferimento a un componente SDK interno utilizzando l’ API visualizzatore `getComponent()` e quindi utilizzi tutta la flessibilità delle API dell’SDK stesso.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti SDK dipende dall’ambiente in cui opera il visualizzatore. Se il visualizzatore è in esecuzione in AEM (Adobe Experience Manager), il visualizzatore carica i componenti SDK nello spazio dei nomi `s7viewers.s7sdk` . E il visualizzatore servito da Dynamic Media Classic carica l&#39;SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato dall’SDK all’interno del visualizzatore ha `s7viewers` o `s7classic` come prefisso. Inoltre, è diverso dallo spazio dei nomi semplice `s7sdk` utilizzato nella Guida utente SDK o nella documentazione API SDK.

Per questo motivo è importante utilizzare uno spazio dei nomi SDK completo quando scrivi un codice di applicazione personalizzato che comunica con i componenti del visualizzatore interni.

Ad esempio, se prevedi di ascoltare l’evento `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene servito da AEM, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e il codice del listener di eventi è simile al seguente:

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
   carouselView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
