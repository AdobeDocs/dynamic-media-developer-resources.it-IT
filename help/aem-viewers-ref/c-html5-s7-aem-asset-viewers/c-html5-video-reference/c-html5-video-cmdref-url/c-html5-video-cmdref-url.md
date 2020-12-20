---
description: Documentazione di riferimento dei comandi per il visualizzatore video.
seo-description: Documentazione di riferimento dei comandi per il visualizzatore video.
seo-title: Riferimento comando - URL
solution: Experience Manager
title: Riferimento comando - URL
topic: Dynamic media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: 3266e8682711dac379a09a0e992d33b8ffc7b5a4
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# Riferimento comando - URL{#command-reference-url}

Documentazione di riferimento dei comandi per il visualizzatore video.

Potete impostare qualsiasi comando di configurazione nell’URL. In alternativa, potete utilizzare i metodi API `setParam()`, `setParams()` o entrambi per impostare qualsiasi comando di configurazione. Potete inoltre specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

Potete assegnare un prefisso ad alcuni comandi di configurazione con il nome della classe o con il nome dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API. La documentazione include prefissi facoltativi per tali comandi. Ad esempio, `playback` è documentato come segue:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

che significa che questo comando viene utilizzato nel modo seguente:

* `playback` (sintassi breve)
* `VideoPlayer.playback` (qualificato con nome classe componente)
* `cont_videoPlayer.playback` (qualificato con ID componente, partendo dal presupposto che  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Consultate anche [Riferimento al comando comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
