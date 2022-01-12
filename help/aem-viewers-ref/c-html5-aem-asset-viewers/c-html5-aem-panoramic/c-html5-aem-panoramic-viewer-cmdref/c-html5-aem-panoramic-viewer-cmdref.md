---
title: Riferimento comando - Attributi di configurazione
description: Documentazione degli attributi di configurazione per il visualizzatore panoramico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione degli attributi di configurazione per il visualizzatore panoramico.

Qualsiasi comando di configurazione può essere impostato in URL o utilizzando `setParam()` e/o `setParams()` Metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome di classe o di istanza del componente SDK HTML5 corrispondente. Un nome di istanza del componente è dinamico e dipende dall’ID dell’elemento DOM del contenitore del visualizzatore passato a `setContainerId()` Metodo API. La documentazione includerà il prefisso facoltativo per tali comandi. Ad esempio: `vrrender` Il comando è documentato come segue:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Ciò significa che questo comando viene utilizzato nel modo seguente:

* `vrrender` (sintassi breve)
* `PanoramicView.vrrender` (qualificato con il nome della classe del componente)
* `cont_panoramicView.vrrender` (qualificato con ID componente, purché cont sia l’ID dell’elemento contenitore)


Vedi [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Vedi [Riferimento comando comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
