---
description: Documentazione degli attributi di configurazione per il visualizzatore video interattivo.
seo-description: Documentazione degli attributi di configurazione per il visualizzatore video interattivo.
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
uuid: eaf7a1a2-b0ec-4df2-926b-5e2c4cd0b3d1
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore video interattivo.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando i metodi API `setParam()`, `setParams()` o entrambi. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome di classe o di istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API . La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `playback` è documentato come segue:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

che significa che è possibile utilizzare questo comando come:

* `playback` (sintassi breve)
* `VideoPlayer.playback` (qualificato con il nome della classe del componente)
* `cont_videoPlayer.playback` (qualificato con ID componente, supponendo che  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
