---
title: Riferimento comando - Attributi di configurazione
description: Documentazione sugli attributi di configurazione per il visualizzatore panoramico.
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2: id: beaff0dd-a904-4c6b-8290-b527cd877d75id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

Documentazione sugli attributi di configurazione per il visualizzatore panoramico.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando i metodi API `setParam()` e/o `setParams()`. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome della classe o dell&#39;istanza del componente SDK di HTML5 corrispondente. Il nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo API `setContainerId()`. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `vrrender` è documentato come segue:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Ciò significa che questo comando viene utilizzato nel modo seguente:

* `vrrender` (sintassi breve)
* `PanoramicView.vrrender` (qualificato con il nome della classe del componente)
* `cont_panoramicView.vrrender` (qualificato con ID componente, supponendo che cont sia l&#39;ID dell&#39;elemento contenitore)


Vedi [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Vedi [Riferimento comando comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
