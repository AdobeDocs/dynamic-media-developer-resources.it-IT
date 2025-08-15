---
title: Spazio dei nomi SDK per visualizzatori
description: Spazio dei nomi SDK per visualizzatori
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b61a17-f9ae-4e71-bd78-276674193044
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Spazio dei nomi SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti del Visualizzatore SDK. Di solito, la pagina web non deve interagire direttamente con l’API dei componenti di SDK; tutte le esigenze comuni sono coperte nell’API del visualizzatore stessa.

Tuttavia, alcuni casi d&#39;uso avanzati richiedono che la pagina web faccia riferimento a un componente interno di SDK utilizzando l&#39;API del visualizzatore `getComponent()` e quindi utilizzi tutta la flessibilità delle API di SDK stessa.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti di SDK dipende dall’ambiente in cui il visualizzatore opera. Se il visualizzatore è in esecuzione in Adobe Experience Manager, carica i componenti SDK nello spazio dei nomi `s7viewers.s7sdk`. Analogamente, il visualizzatore fornito da Dynamic Media Classic carica il SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato da SDK nel visualizzatore ha `s7viewers` o `s7classic` come prefisso. Inoltre, è diverso dal normale spazio dei nomi `s7sdk` utilizzato nella Guida utente di SDK o nella documentazione API di SDK.

Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando si scrive codice personalizzato dell’applicazione che comunica con i componenti interni del visualizzatore.

Se ad esempio si intende ascoltare l&#39;evento `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene fornito da Experience Manager, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e il codice del listener di eventi è simile al seguente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
