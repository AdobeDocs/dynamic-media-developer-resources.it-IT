---
title: Spazio dei nomi SDK per visualizzatori
description: Spazio dei nomi SDK per visualizzatori
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 1712f08c-70e6-483e-a4e5-614448f35374
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Spazio dei nomi SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti SDK per visualizzatori. Di solito, la pagina web non deve interagire direttamente con l’API dei componenti SDK; tutte le esigenze comuni sono coperte nell’API del visualizzatore stessa.

Tuttavia, alcuni casi d&#39;uso avanzati richiedono che la pagina web faccia riferimento a un componente SDK interno utilizzando l&#39;API del visualizzatore `getComponent()` e quindi utilizzi tutta la flessibilità delle API dell&#39;SDK stesso.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti SDK dipende dall’ambiente in cui opera il visualizzatore. Se il visualizzatore è in esecuzione in Adobe Experience Manager, carica i componenti SDK nello spazio dei nomi `s7viewers.s7sdk`. Il visualizzatore fornito da Dynamic Media Classic carica l&#39;SDK in `s7classic.s7sdk`.

In entrambi i casi, il prefisso dello spazio dei nomi utilizzato dall&#39;SDK nel visualizzatore è `s7viewers` o `s7classic`. Inoltre, è diverso dal normale spazio dei nomi `s7sdk` utilizzato nella Guida utente SDK o nella documentazione API SDK.

Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando scrivi codice personalizzato dell’applicazione che comunica con i componenti interni del visualizzatore.

Se, ad esempio, si intende ascoltare l&#39;evento `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene servito da Experience Manager, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e il codice del listener di eventi è simile al seguente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var carouselView = <instance>.getComponent("carouselView"); 
   carouselView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
