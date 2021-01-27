---
description: Spazio dei nomi SDK per visualizzatori
solution: Experience Manager
title: Spazio dei nomi SDK per visualizzatori
topic: Dynamic Media
uuid: 993547f2-b943-4aba-b6cc-54fa32cfb2d3
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# Spazio dei nomi SDK del visualizzatore{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Nella maggior parte dei casi, la pagina Web non deve interagire direttamente con l’API dei componenti SDK; tutte le esigenze comuni sono coperte dall&#39;API del visualizzatore stessa.

Tuttavia, alcuni casi d&#39;uso avanzati richiedono che la pagina Web ottenga un riferimento a un componente SDK interno utilizzando l&#39;API del visualizzatore `getComponent()`, quindi utilizzi tutta la flessibilità delle API dell&#39;SDK stesso.

Lo spazio dei nomi utilizzato per caricare e inizializzare i componenti SDK dal visualizzatore dipende dall&#39;ambiente in cui funziona il visualizzatore. Se il visualizzatore è in esecuzione in AEM (Adobe Experience Manager), il visualizzatore carica i componenti SDK nello spazio dei nomi `s7viewers.s7sdk`. Inoltre, il visualizzatore distribuito da Dynamic Media Classic carica l&#39;SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio nomi utilizzato dall&#39;SDK all&#39;interno del visualizzatore ha il prefisso `s7viewers` o `s7classic`. Inoltre, è diverso dallo spazio dei nomi semplice `s7sdk` utilizzato nella guida utente dell&#39;SDK o nella documentazione dell&#39;API SDK.

Per questo motivo è importante utilizzare uno spazio dei nomi SDK completo quando si crea un codice applicazione personalizzato che comunica con i componenti del visualizzatore interno.

Ad esempio, se prevedete di ascoltare l&#39;evento `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene servito da AEM, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e il codice del listener di eventi è simile a quello seguente:

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

