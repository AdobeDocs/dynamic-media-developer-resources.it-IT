---
description: Documentazione degli attributi di configurazione per il visualizzatore di immagini interattive.
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Immagini interattive
role: Developer,Business Practitioner
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore di immagini interattive.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando i metodi API `setParam()`, `setParams()` o entrambi. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome di classe o di istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API . La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `zoomstep` è documentato come segue:

`[ZoomView.|<containerId>_zoomView].fmt`

che significa che è possibile utilizzare questo comando come:

* `fmt` (sintassi breve)
* `ZoomView.fmt` (qualificato con il nome della classe del componente)
* `cont_zoomView.fmt` (qualificato con ID componente, supponendo che  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
