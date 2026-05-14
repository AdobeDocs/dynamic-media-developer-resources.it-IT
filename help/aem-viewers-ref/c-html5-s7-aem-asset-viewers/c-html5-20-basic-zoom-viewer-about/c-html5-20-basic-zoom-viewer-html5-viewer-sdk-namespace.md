---
title: Spazio dei nomi SDK per visualizzatori
description: Spazio dei nomi SDK per visualizzatori
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4ccdf8c2-6cf5-4cb3-af61-fab50f410566
TQID: 'https://experienceleague.adobe.com/LKnfgvH5ndVKqJNXLLY7BnB-AQbVFNrWnumcoDjfNQI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 221
ht-degree: 0%

---

# Spazio dei nomi SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti del Visualizzatore SDK. Di solito, la pagina web non deve interagire direttamente con l’API dei componenti di SDK; tutte le esigenze comuni sono coperte nell’API del visualizzatore stessa.

Tuttavia, alcuni casi d&#39;uso avanzati richiedono che la pagina web faccia riferimento a un componente interno di SDK utilizzando l&#39;API del visualizzatore `getComponent()` e quindi utilizzi tutta la flessibilità delle API di SDK stessa.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti di SDK dipende dall’ambiente in cui il visualizzatore opera. Se il visualizzatore è in esecuzione in Adobe Experience Manager, carica i componenti SDK nello spazio dei nomi `s7viewers.s7sdk`. Il visualizzatore fornito da Dynamic Media Classic carica il SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato da SDK nel visualizzatore ha `s7viewers` o `s7classic` come prefisso. Inoltre, è diverso dal normale spazio dei nomi `s7sdk` utilizzato nella Guida utente di SDK o nella documentazione API di SDK.

Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando si scrive codice personalizzato dell’applicazione che comunica con i componenti interni del visualizzatore.

Se ad esempio si intende ascoltare l&#39;evento `StatusEvent.NOTF_VIEW_READY` e il visualizzatore è gestito da Experience Manager, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e il codice del listener di eventi è simile al seguente:

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
