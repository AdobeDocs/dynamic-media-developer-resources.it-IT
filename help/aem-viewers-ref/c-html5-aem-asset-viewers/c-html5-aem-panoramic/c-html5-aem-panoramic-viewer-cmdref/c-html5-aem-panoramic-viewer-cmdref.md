---
title: Riferimento comando - Attributi di configurazione
description: Documentazione sugli attributi di configurazione per il visualizzatore panoramico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione sugli attributi di configurazione per il visualizzatore panoramico.

Qualsiasi comando di configurazione può essere impostato in URL o utilizzando `setParam()` e/o `setParams()` Metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome della classe o dell’istanza del componente SDK HTML5 corrispondente. Il nome di un&#39;istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore trasmesso a `setContainerId()` metodo API. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio: `vrrender` il comando è documentato come segue:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Ciò significa che questo comando viene utilizzato nel modo seguente:

* `vrrender` (sintassi breve)
* `PanoramicView.vrrender` (qualificato con il nome della classe del componente)
* `cont_panoramicView.vrrender` (qualificato con ID componente, supponendo che cont sia l’ID dell’elemento contenitore)


Consulta [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulta [Riferimento comando comune a tutti i visualizzatori - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
