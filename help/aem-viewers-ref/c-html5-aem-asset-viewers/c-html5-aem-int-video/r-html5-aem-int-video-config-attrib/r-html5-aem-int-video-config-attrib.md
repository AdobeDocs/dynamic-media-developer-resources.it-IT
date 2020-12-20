---
description: Documentazione degli attributi di configurazione per il visualizzatore video interattivo.
seo-description: Documentazione degli attributi di configurazione per il visualizzatore video interattivo.
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
topic: Dynamic media
uuid: eaf7a1a2-b0ec-4df2-926b-5e2c4cd0b3d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore video interattivo.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando i metodi API `setParam()`, `setParams()` o entrambi. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono avere un prefisso con il nome della classe o dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `playback` è documentato come segue:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

questo significa che puoi usare questo comando come:

* `playback` (sintassi breve)
* `VideoPlayer.playback` (qualificato con nome classe componente)
* `cont_videoPlayer.playback` (con ID componente, supponendo  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
