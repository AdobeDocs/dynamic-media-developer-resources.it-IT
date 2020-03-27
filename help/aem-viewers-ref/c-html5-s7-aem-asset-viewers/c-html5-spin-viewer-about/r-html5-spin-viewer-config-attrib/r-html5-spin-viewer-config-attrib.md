---
description: Documentazione degli attributi di configurazione per il visualizzatore 360 gradi.
seo-description: Documentazione degli attributi di configurazione per il visualizzatore 360 gradi.
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
topic: Dynamic media
uuid: ba60da44-d30d-459f-b3d8-5cf3ea4bcbdb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore 360 gradi.

Qualsiasi comando di configurazione può essere impostato in URL o utilizzando `setParam()`o `setParams()`, o entrambi, metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono avere un prefisso con il nome della classe o dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, `zoomstep` il comando è documentato come segue:

`[SpinView.|<containerId>_spinView].zoomstep`

questo significa che puoi usare questo comando come:

* `zoomstep` (sintassi breve)
* `SpinView.zoomstep` (qualificato con nome classe componente)
* `cont_spinView.zoomstep` (con ID componente, supponendo `cont` sia l’ID dell’elemento contenitore)

Consultate anche Riferimento [comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
