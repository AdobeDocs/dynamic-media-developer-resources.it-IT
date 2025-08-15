---
title: Riferimento Comando – Attributi di configurazione
description: Documentazione sugli attributi di configurazione per visualizzatore 360 gradi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Riferimento Comando – Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione sugli attributi di configurazione per visualizzatore 360 gradi.

Qualsiasi comando di configurazione può essere impostato in URL o utilizzando `setParam()`, o `setParams()`, o entrambi, i metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome della classe o dal nome istanza del componente SDK del visualizzatore corrispondente. Un nome istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM contenitore visualizzatore passato al `setContainerId()` metodo API. Documentazione include un prefisso facoltativo per tali comandi. Ad esempio, `zoomstep` il comando è documentato come segue:

`[SpinView.|<containerId>_spinView].zoomstep`

Ciò significa che è possibile utilizzare questo comando come segue

* `zoomstep` (sintassi breve)
* `SpinView.zoomstep` (qualificato con il nome della classe componente)
* `cont_spinView.zoomstep` (qualificato con ID componente, supponendo `cont` che sia l&#39;ID dell&#39;elemento contenitore)

Vedere anche [Comando riferimento comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
