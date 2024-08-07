---
title: Riferimento comando - URL
description: Documentazione di riferimento sui comandi per Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Riferimento comando - URL{#command-reference-url}

Documentazione di riferimento sui comandi per Video360 Viewer.

Puoi impostare qualsiasi comando di configurazione nell’URL. In alternativa, è possibile utilizzare i metodi API `setParam()`, `setParams()` o entrambi per impostare qualsiasi comando di configurazione. Puoi anche specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

Ad alcuni comandi di configurazione è possibile anteporre il nome della classe o dell&#39;istanza del componente SDK HTML5 Viewer corrispondente. Il nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo API `setContainerId()`. La documentazione include prefissi facoltativi per tali comandi. Ad esempio, `playback` è documentato come segue:

```
[Video360Player.|<containerId>_video360Player].playback
```

Ciò significa che questo comando viene utilizzato nel modo seguente:

* `playback` (sintassi breve)
* `Video360Player.playback` (qualificato con il nome della classe del componente)
* `cont_video360Player.playback` (qualificato con ID componente, supponendo che `cont` sia l&#39;ID dell&#39;elemento contenitore)

Vedi [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento al comando comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
