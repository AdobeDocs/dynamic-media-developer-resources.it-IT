---
description: Documentazione degli attributi di configurazione per il visualizzatore video.
seo-description: Documentazione degli attributi di configurazione per il visualizzatore video.
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
topic: Dynamic media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore video.

Potete impostare qualsiasi comando di configurazione nell’URL. In alternativa, potete utilizzare i metodi API `setParam()`, `setParams()` o entrambi per impostare qualsiasi comando di configurazione. Potete inoltre specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

Potete assegnare un prefisso ad alcuni comandi di configurazione con il nome della classe o con il nome dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API. La documentazione include prefissi facoltativi per tali comandi. Ad esempio, `playback` è documentato come segue:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

che significa che questo comando viene utilizzato nel modo seguente:

* `playback` (sintassi breve)
* `VideoPlayer.playback` (qualificato con nome classe componente)
* `cont_videoPlayer.playback` (qualificato con ID componente, partendo dal presupposto che  `cont` sia l’ID dell’elemento contenitore)

Vedere [Riferimento comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consultate [Riferimento comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
