---
description: Documentazione di riferimento dei comandi per il visualizzatore Video360.
solution: Experience Manager
title: Riferimento comando - URL
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Developer,Business Practitioner
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Riferimento comando - URL{#command-reference-url}

Documentazione di riferimento dei comandi per il visualizzatore Video360.

Puoi impostare qualsiasi comando di configurazione nell’URL. In alternativa, puoi utilizzare i metodi API `setParam()` o `setParams()` o entrambi per impostare qualsiasi comando di configurazione. Puoi anche specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

È possibile assegnare un prefisso ad alcuni comandi di configurazione con il nome della classe o il nome dell’istanza del componente SDK per visualizzatori HTML5 corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API . La documentazione include prefissi facoltativi per tali comandi. Ad esempio, `playback` è documentato come segue:

```
[Video360Player.|<containerId>_video360Player].playback
```

che significa che questo comando viene utilizzato nel modo seguente:

* `playback` (sintassi breve)
* `Video360Player.playback` (qualificato con il nome della classe del componente)
* `cont_video360Player.playback` (qualificato con ID componente, supponendo che  `cont` sia l’ID dell’elemento contenitore)

Consulta [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento ai comandi comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
