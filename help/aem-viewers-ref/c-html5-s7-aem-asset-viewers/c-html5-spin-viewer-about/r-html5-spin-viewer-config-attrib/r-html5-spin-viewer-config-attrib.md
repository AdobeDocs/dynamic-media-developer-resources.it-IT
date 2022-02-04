---
title: Riferimento comando - Attributi di configurazione
description: Documentazione degli attributi di configurazione per il visualizzatore a 360 gradi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore a 360 gradi.

Qualsiasi comando di configurazione può essere impostato in URL o utilizzando `setParam()`oppure `setParams()`, o entrambi, i metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome di classe o di istanza del componente SDK per visualizzatori corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato a `setContainerId()` Metodo API. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio: `zoomstep` Il comando è documentato come segue:

`[SpinView.|<containerId>_spinView].zoomstep`

Ciò significa che è possibile utilizzare questo comando come segue

* `zoomstep` (sintassi breve)
* `SpinView.zoomstep` (qualificato con il nome della classe del componente)
* `cont_spinView.zoomstep` (qualificato con ID componente, supponendo che `cont` è l&#39;ID dell&#39;elemento contenitore)

Vedi anche [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
