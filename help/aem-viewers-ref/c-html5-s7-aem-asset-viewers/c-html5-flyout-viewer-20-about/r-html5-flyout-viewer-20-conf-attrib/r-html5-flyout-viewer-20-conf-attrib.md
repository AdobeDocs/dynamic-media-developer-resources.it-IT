---
description: Documentazione degli attributi di configurazione per il visualizzatore a comparsa
seo-description: Documentazione degli attributi di configurazione per il visualizzatore a comparsa
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
uuid: d7e89a24-a235-4f20-86d1-25aacd118880
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore a comparsa

Puoi impostare qualsiasi comando di configurazione nell’URL. In alternativa, puoi utilizzare `setParam()`, `setParams()` o entrambi i metodi API. Puoi inoltre specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

Alcuni comandi di configurazione hanno il prefisso nome della classe o dell’istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API . La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `zoomfactor` è documentato come segue:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Il comando viene utilizzato come segue:

* `zoomfactor` (sintassi breve)
* `FlyoutZoomView.zoomfactor` (qualificato con un nome di classe di un componente)
* `cont_flyout.zoomfactor` (qualificato con l’ID del componente, supponendo che  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
