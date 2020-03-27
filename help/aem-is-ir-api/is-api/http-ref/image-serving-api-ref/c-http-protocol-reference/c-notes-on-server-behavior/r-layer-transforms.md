---
description: Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.
seo-description: Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.
seo-title: Trasformazioni dei livelli
solution: Experience Manager
title: Trasformazioni dei livelli
topic: Scene7 Image Serving - Image Rendering API
uuid: b32b5af4-66ad-474a-9bca-4b6da8f43bf9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Trasformazioni dei livelli{#layer-transforms}

Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.

Le seguenti operazioni vengono applicate alle immagini sorgente, nell’ordine indicato, per ottenere la relazione spaziale desiderata con il livello 0:

1. Applica `crop=`, se specificato.
1. Scala basata su `size=` o, se non `size=` è specificato, basata su `scale=`oppure, se non `scale=` è specificato, su `res=`oppure, se non `res=`è specificato, utilizza l&#39;immagine sorgente a risoluzione piena.
1. Applica `flip=`, se specificato.
1. Applica `rotate=`, se specificato.
1. Applica `extend=`, se specificato.
1. Posizionate il livello nel quadro in base a `origin=` e `pos=` (vedete di seguito).

Le seguenti trasformazioni sono applicate ai livelli di testo:

1. Le dimensioni della casella di testo sono determinate da `size=`o da larghezza e altezza del testo, se `size=` sono fornite solo parzialmente o per nulla. Il testo è allineato all’interno della casella di testo utilizzando gli attributi di allineamento del testo rtf. Il testo può essere ritagliato dalla casella di testo.
1. Consente di ridimensionare il contenuto del testo in base alla risoluzione specificata con `textAttr=`.
1. Applica `rotate=`, se specificato.
1. Applica `extend=`, se specificato.
1. Posizionate il livello nel quadro in base a `origin=` e `pos=`(vedete di seguito).

Per i livelli di immagine e testo, l’ultimo passaggio del posizionamento del livello nel quadro non si applica al livello 0, poiché il livello 0 costituisce effettivamente il quadro.
