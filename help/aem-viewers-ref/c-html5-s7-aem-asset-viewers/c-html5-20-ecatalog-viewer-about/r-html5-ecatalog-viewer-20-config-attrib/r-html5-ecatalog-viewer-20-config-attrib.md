---
description: Documentazione degli attributi di configurazione per il visualizzatore di eCatalog.
seo-description: Documentazione degli attributi di configurazione per il visualizzatore di eCatalog.
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
topic: Dynamic media
uuid: 823ad411-653a-44de-97de-147e3b27a917
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore di eCatalog.

Qualsiasi comando di configurazione può essere impostato in URL o utilizzando `setParam()`o `setParams()`, o entrambi, metodi API. Potete inoltre specificare qualsiasi attributo di configurazione specificato nel record di configurazione lato server.

Per alcuni comandi di configurazione, potete inserirli in un prefisso con il nome della classe o dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API. La documentazione include il prefisso facoltativo per tali comandi. Ad esempio, `zoomstep` il comando è documentato come segue:

`[PageView.|<containerId>_pageView].zoomstep`

questo significa che puoi usare questo comando come:

* `zoomstep` (sintassi breve)
* `PageView.zoomstep` (qualificato con nome classe componente)
* `cont_pageView.zoomstep` (con ID componente, supponendo `cont` sia l’ID dell’elemento contenitore)

Consultate anche Riferimento [comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
