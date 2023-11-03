---
title: Riferimento comando - Attributi di configurazione
description: Documentazione sugli attributi di configurazione per il visualizzatore di file multimediali diversi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione sugli attributi di configurazione per il visualizzatore di file multimediali diversi.

Qualsiasi comando di configurazione può essere impostato in URL o utilizzando `setParam()`, o `setParams()`, o entrambi, i metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome della classe o dell’istanza del componente SDK del visualizzatore corrispondente. Il nome di un&#39;istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore trasmesso a `setContainerId()` metodo API. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio: `zoomstep` il comando è documentato come segue:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Ciò significa che è possibile utilizzare questo comando nel modo seguente

* `zoomstep` (sintassi breve)
* `ZoomView.zoomstep` (qualificato con il nome della classe del componente)
* `cont_zoomView.zoomstep` (qualificato con ID componente, supponendo `cont` è l’ID dell’elemento contenitore)

Vedi anche [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
