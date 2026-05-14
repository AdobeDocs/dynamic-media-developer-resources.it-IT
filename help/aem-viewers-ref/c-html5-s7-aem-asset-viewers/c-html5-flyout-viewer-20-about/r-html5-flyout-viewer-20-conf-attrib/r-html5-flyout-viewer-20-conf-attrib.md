---
title: Riferimento comando - Attributi di configurazione
description: Documentazione sugli attributi di configurazione per il visualizzatore a comparsa
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
TQID: 'https://experienceleague.adobe.com/Bus1MH5Y8xppGXxnARx0Fq11dslSbY9Q7yAlFtF6KzI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione sugli attributi di configurazione per il visualizzatore a comparsa

Puoi impostare qualsiasi comando di configurazione nell’URL. In alternativa, è possibile utilizzare `setParam()`, `setParams()` o entrambi i metodi API. È inoltre possibile specificare qualsiasi attributo di configurazione nel record di configurazione lato server.

Alcuni comandi di configurazione sono preceduti dal nome della classe o dell&#39;istanza del componente Viewer SDK corrispondente. Il nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo API `setContainerId()`. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `zoomfactor` è documentato come segue:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

Il comando viene utilizzato come segue:

* `zoomfactor` (sintassi breve)
* `FlyoutZoomView.zoomfactor` (qualificato con un nome di classe di componente)
* `cont_flyout.zoomfactor` (qualificato con l&#39;ID componente, supponendo che `cont` sia l&#39;ID dell&#39;elemento contenitore)

Vedi anche [Riferimento comando comune a tutti i visualizzatori - Attributi configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
