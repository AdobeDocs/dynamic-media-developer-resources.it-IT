---
description: Documentazione degli attributi di configurazione per il visualizzatore di eCatalog.
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore di eCatalog.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando i metodi API `setParam()`, `setParams()` o entrambi. Puoi inoltre specificare qualsiasi attributo di configurazione specificato nel record di configurazione lato server.

Per alcuni comandi di configurazione puoi usare il prefisso con il nome della classe o dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API . La documentazione include il prefisso facoltativo per tali comandi. Ad esempio, il comando `zoomstep` è documentato come segue:

`[PageView.|<containerId>_pageView].zoomstep`

che significa che è possibile utilizzare questo comando come:

* `zoomstep` (sintassi breve)
* `PageView.zoomstep` (qualificato con il nome della classe del componente)
* `cont_pageView.zoomstep` (qualificato con ID componente, supponendo che  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
