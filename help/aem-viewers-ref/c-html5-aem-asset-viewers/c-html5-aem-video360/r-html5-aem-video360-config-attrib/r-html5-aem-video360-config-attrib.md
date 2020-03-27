---
description: Documentazione degli attributi di configurazione per il visualizzatore Video360.
seo-description: Documentazione degli attributi di configurazione per il visualizzatore Video360.
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
topic: Dynamic media
uuid: 645bba87-3d84-46e9-97fc-7019c5dd87ca
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore Video360.

Qualsiasi comando di configurazione può essere impostato in URL o utilizzando `setParam()`o `setParams()`, o entrambi, metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono avere un prefisso con il nome della classe o dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, `playback` il comando è documentato come segue:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

questo significa che puoi usare questo comando come:

* `playback` (sintassi breve)
* `VideoPlayer.playback` (qualificato con nome classe componente)
* `cont_videoPlayer.playback` (con ID componente, supponendo `cont` sia l’ID dell’elemento contenitore)

Consultate anche Riferimento [comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
