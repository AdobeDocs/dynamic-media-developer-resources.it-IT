---
title: Riferimento comando - URL
description: Documentazione di riferimento dei comandi per Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Riferimento comando - URL{#command-reference-url}

Documentazione di riferimento dei comandi per Smart Crop Video Viewer.

Puoi impostare qualsiasi comando di configurazione nell’URL. In alternativa, puoi utilizzare i metodi API `setParam()`oppure `setParams()`o entrambi per impostare qualsiasi comando di configurazione. Puoi anche specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

È possibile usare il prefisso di alcuni comandi di configurazione con il nome della classe o con il nome dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato a `setContainerId()` Metodo API. La documentazione include prefissi facoltativi per tali comandi. Ad esempio: `playback` è documentato come segue:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Ciò significa che questo comando viene utilizzato nel modo seguente:

* `playback` (sintassi breve)
* `SmartCropVideoPlayer.playback` (qualificato con il nome della classe del componente)
* `cont_smartCropVideoPlayer.playback` (qualificato con ID componente, partendo dal presupposto che `cont` è l&#39;ID dell&#39;elemento contenitore)

Vedi anche [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Vedi anche [Riferimento comando comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
