---
title: Spazio dei nomi SDK per visualizzatori
description: Spazio dei nomi SDK per visualizzatori
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6cbf7eef-0d17-4411-9a74-22455009f66d
TQID: 'https://experienceleague.adobe.com/jP-ctDVghPscHD19iQPa4s5GnTyXKIIFOFu4UJTFo98'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%
---
# Spazio dei nomi SDK per visualizzatori{#viewer-sdk-namespace}

Il visualizzatore è costituito da molti componenti del Visualizzatore SDK. Di solito, la pagina web non deve interagire direttamente con l’API dei componenti di SDK; tutte le esigenze comuni sono coperte nell’API del visualizzatore stessa.

Tuttavia, alcuni casi d&#39;uso avanzati richiedono che la pagina web faccia riferimento a un componente interno di SDK utilizzando l&#39;API del visualizzatore `getComponent()` e quindi utilizzi tutta la flessibilità delle API di SDK stessa.

Lo spazio dei nomi utilizzato dal visualizzatore per caricare e inizializzare i componenti di SDK dipende dall’ambiente in cui il visualizzatore opera. Se il visualizzatore è in esecuzione in Adobe Experience Manager, carica i componenti SDK nello spazio dei nomi `s7viewers.s7sdk`. Analogamente, il visualizzatore fornito da Dynamic Media Classic carica il SDK in `s7classic.s7sdk`.

In entrambi i casi, lo spazio dei nomi utilizzato da SDK nel visualizzatore ha `s7viewers` o `s7classic` come prefisso. Inoltre, è diverso dal normale spazio dei nomi `s7sdk` utilizzato nella Guida utente di SDK o nella documentazione API di SDK. Per questo motivo, è importante utilizzare uno spazio dei nomi SDK completo quando si scrive codice personalizzato dell’applicazione che comunica con i componenti interni del visualizzatore.

Se ad esempio si intende ascoltare l&#39;evento `StatusEvent.NOTF_VIEW_READY` e il visualizzatore viene fornito da Experience Manager, il tipo di evento completo è `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` e il codice del listener di eventi è simile al seguente:

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var smartCropVideoPlayer = <instance>.getComponent("smartCropVideoPlayer"); 
   smartCropVideoPlayer.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
