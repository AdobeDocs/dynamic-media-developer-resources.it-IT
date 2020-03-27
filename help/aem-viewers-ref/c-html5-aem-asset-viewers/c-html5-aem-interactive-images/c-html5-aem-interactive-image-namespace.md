---
description: 'null'
seo-description: 'null'
seo-title: Spazio dei nomi SDK per visualizzatori
solution: Experience Manager
title: Spazio dei nomi SDK per visualizzatori
topic: Dynamic media
uuid: e1639806-3052-4913-aae0-ca9a79100d0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Spazio dei nomi SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Nella maggior parte dei casi, la pagina Web non deve interagire direttamente con l’API dei componenti SDK; tutte le esigenze comuni sono coperte dall&#39;API del visualizzatore stessa.

Tuttavia, alcuni casi d’uso avanzati richiedono che la pagina Web ottenga un riferimento a un componente SDK interno utilizzando l’API `getComponent()` visualizzatore e quindi utilizzi tutta la flessibilità delle API dell’SDK stesso.

Lo spazio dei nomi utilizzato per caricare e inizializzare i componenti SDK dal visualizzatore dipende dall&#39;ambiente in cui funziona il visualizzatore. Se il visualizzatore è in esecuzione in AEM (Adobe Experience Manager), il visualizzatore carica i componenti SDK nello `s7viewers.s7sdk` spazio dei nomi. Il visualizzatore fornito da Scene7 Publishing System carica l’SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio nomi usato dall’SDK all’interno del visualizzatore ha `s7viewers` o `s7classic` come prefisso. Inoltre, è diverso dallo `s7sdk` spazio dei nomi semplice utilizzato nella Guida utente dell’SDK o nella documentazione dell’API SDK.

Per questo motivo è importante utilizzare uno spazio dei nomi SDK completo quando si crea un codice applicazione personalizzato che comunica con i componenti del visualizzatore interno.

Ad esempio, se prevedete di ascoltare l&#39; `StatusEvent.NOTF_VIEW_READY` evento e il visualizzatore viene servito da AEM, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`e il codice del listener di eventi è simile al seguente:

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

