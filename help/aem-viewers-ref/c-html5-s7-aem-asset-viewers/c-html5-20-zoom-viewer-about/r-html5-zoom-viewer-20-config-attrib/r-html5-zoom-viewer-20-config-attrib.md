---
title: Riferimento comando - Attributi di configurazione
description: Documentazione sugli attributi di configurazione per Visualizzatore zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
TQID: 'https://experienceleague.adobe.com/34VqWl1GOWOG7G8vXJIpc7NH4w26x2NOGO3yG2yknyc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione sugli attributi di configurazione per Visualizzatore zoom.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando `setParam()`, `setParams()` o entrambi i metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome della classe o dell&#39;istanza del componente Viewer SDK corrispondente. Il nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo API `setContainerId()`. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `zoomstep` è documentato come segue:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Ciò significa che è possibile utilizzare il comando come

* `zoomstep` (sintassi breve)
* `ZoomView.zoomstep` (qualificato con il nome della classe del componente)
* `cont_zoomView.zoomstep` (qualificato con ID componente, supponendo che `cont` sia l&#39;ID dell&#39;elemento contenitore)

Vedi anche [Riferimento comando comune a tutti i visualizzatori - Attributi configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
