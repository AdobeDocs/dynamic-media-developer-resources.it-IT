---
title: Riferimento comando - Attributi di configurazione
description: Documentazione sugli attributi di configurazione per il visualizzatore eCatalog.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione sugli attributi di configurazione per il visualizzatore eCatalog.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando `setParam()`, `setParams()` o entrambi i metodi API. È inoltre possibile specificare qualsiasi attributo di configurazione specificato nel record di configurazione lato server.

Per alcuni comandi di configurazione, è possibile aggiungervi il prefisso con il nome della classe o dell&#39;istanza del componente Viewer SDK corrispondente. Il nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo API `setContainerId()`. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `zoomstep` è documentato come segue:

`[PageView.|<containerId>_pageView].zoomstep`

Ciò significa che è possibile utilizzare questo comando come

* `zoomstep` (sintassi breve)
* `PageView.zoomstep` (qualificato con il nome della classe del componente)
* `cont_pageView.zoomstep` (qualificato con ID componente, supponendo che `cont` sia l&#39;ID dell&#39;elemento contenitore)

Vedi anche [Riferimento comando comune a tutti i visualizzatori - Attributi configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
