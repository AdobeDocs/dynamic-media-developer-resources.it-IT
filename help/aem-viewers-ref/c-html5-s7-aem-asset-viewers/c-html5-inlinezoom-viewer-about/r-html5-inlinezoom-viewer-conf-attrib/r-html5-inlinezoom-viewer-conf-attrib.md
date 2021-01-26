---
description: Documentazione degli attributi di configurazione per il visualizzatore a comparsa
seo-description: Documentazione degli attributi di configurazione per il visualizzatore a comparsa
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
topic: Dynamic Media
uuid: 0813c334-37b7-43af-b39d-bec66658ad58
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore a comparsa

Potete impostare qualsiasi comando di configurazione nell’URL. In alternativa, potete utilizzare i metodi `setParam()`, `setParams()` o entrambi i metodi API. Potete inoltre specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

Alcuni comandi di configurazione hanno il prefisso nome classe o nome istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `zoomfactor` è documentato come segue:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Il comando viene utilizzato come segue:

* `zoomfactor` (sintassi breve)
* `FlyoutZoomView.zoomfactor` (qualificato con un nome di classe di componente)
* `cont_flyout.zoomfactor` (qualificato con l’ID del componente, supponendo che  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
