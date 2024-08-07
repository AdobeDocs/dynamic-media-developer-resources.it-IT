---
title: Riferimento comando - Attributi di configurazione
description: Documentazione sugli attributi di configurazione per il visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 80b7971c-82dc-47a2-adde-9e061a0f856d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Documentazione sugli attributi di configurazione per il visualizzatore video interattivo.

Qualsiasi comando di configurazione può essere impostato nell&#39;URL o utilizzando `setParam()`, `setParams()` o entrambi i metodi API. Qualsiasi attributo di configurazione può essere specificato anche nel record di configurazione lato server.

Alcuni comandi di configurazione possono essere preceduti dal nome della classe o dell’istanza del componente SDK del visualizzatore corrispondente. Il nome di istanza del componente è dinamico e dipende dall&#39;ID dell&#39;elemento DOM del contenitore del visualizzatore passato al metodo API `setContainerId()`. La documentazione include un prefisso facoltativo per tali comandi. Ad esempio, il comando `playback` è documentato come segue:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

E significa che puoi utilizzare il seguente comando come:

* `playback` (sintassi breve)
* `VideoPlayer.playback` (qualificato con il nome della classe del componente)
* `cont_videoPlayer.playback` (qualificato con ID componente, supponendo che `cont` sia l&#39;ID dell&#39;elemento contenitore)

Vedi anche [Riferimento comando comune a tutti i visualizzatori - Attributi configurazione](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
