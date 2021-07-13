---
description: Documentazione degli attributi di configurazione per il visualizzatore Carosello.
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,User
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore Carosello.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando i metodi API `setParam()`, `setParams()` o entrambi. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome di classe o di istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato al metodo `setContainerId()` API . La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `zoomstep` è documentato come segue:

`[ZoomView.|<containerId>_carouselView].fmt`

che significa che è possibile utilizzare questo comando come:

* `fmt` (sintassi breve)
* `CarouselView.fmt` (qualificato con il nome della classe del componente)
* `cont_carouselView.fmt` (qualificato con ID componente, supponendo che  `cont` sia l’ID dell’elemento contenitore)

Vedere anche [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
