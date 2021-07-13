---
description: Documentazione di riferimento dei comandi per Visualizzatore video interattivo.
solution: Experience Manager
title: Riferimento comando - URL
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,User
exl-id: e0a9e269-4826-4518-9222-6a833d11746b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Riferimento comando - URL{#command-reference-url}

Documentazione di riferimento dei comandi per Visualizzatore video interattivo.

Puoi impostare qualsiasi comando di configurazione nell’URL. In alternativa, puoi utilizzare i metodi API `setParam()` o `setParams()` o entrambi per impostare qualsiasi comando di configurazione. Puoi anche specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

È possibile usare il prefisso di alcuni comandi di configurazione con il nome della classe o con il nome dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API . La documentazione include prefissi facoltativi per tali comandi. Ad esempio, `playback` è documentato come segue:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

che significa che questo comando viene utilizzato nel modo seguente:

* `playback` (sintassi breve)
* `VideoPlayer.playback` (qualificato con il nome della classe del componente)
* `cont_videoPlayer.playback` (qualificato con ID componente, supponendo che  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Consulta anche [Riferimento ai comandi comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
