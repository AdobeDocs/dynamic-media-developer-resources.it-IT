---
title: Riferimento comando - URL
description: Documentazione di riferimento sui comandi per il visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a9e269-4826-4518-9222-6a833d11746b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Riferimento comando - URL{#command-reference-url}

Documentazione di riferimento sui comandi per il visualizzatore video interattivo.

Puoi impostare qualsiasi comando di configurazione nell’URL. In alternativa, puoi utilizzare i metodi API di `setParam()`, o `setParams()`, o entrambi per impostare qualsiasi comando di configurazione. Puoi anche specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

Ad alcuni comandi di configurazione è possibile aggiungere il nome della classe o dell&#39;istanza del componente SDK del visualizzatore corrispondente. Il nome di un&#39;istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore trasmesso a `setContainerId()` metodo API. La documentazione include prefissi facoltativi per tali comandi. Ad esempio: `playback` è documentato come segue:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Ciò significa che questo comando viene utilizzato nel modo seguente

* `playback` (sintassi breve)
* `VideoPlayer.playback` (qualificato con il nome della classe del componente)
* `cont_videoPlayer.playback` (qualificato con ID componente, supponendo che `cont` è l’ID dell’elemento contenitore)

Vedi anche [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Vedi anche [Riferimento comando comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
