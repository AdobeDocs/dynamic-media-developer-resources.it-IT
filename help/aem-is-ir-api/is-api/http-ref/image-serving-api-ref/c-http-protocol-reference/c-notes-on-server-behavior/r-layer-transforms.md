---
description: Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.
solution: Experience Manager
title: Trasformazioni di livello
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Trasformazioni di livello{#layer-transforms}

Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.

Le seguenti operazioni vengono applicate alle immagini sorgente, nell&#39;ordine specificato, per ottenere la relazione spaziale desiderata con il livello 0:

1. `crop=`Applica , se specificato.
1. Scala in base a `size=` o, se `size=` non è specificato, in base a `scale=`, oppure, se `scale=` non è specificato, in base a `res=`, oppure, se `res=`non è specificato, utilizza l&#39;immagine sorgente a risoluzione massima.
1. `flip=`Applica , se specificato.
1. `rotate=`Applica , se specificato.
1. `extend=`Applica , se specificato.
1. Posizionate il livello nel quadro in base a `origin=` e `pos=` (vedete sotto).

Le seguenti trasformazioni vengono applicate ai livelli di testo:

1. La dimensione della casella di testo è determinata da `size=`, o la larghezza e l&#39;altezza del testo, se `size=` è fornito solo parzialmente o per niente. Il testo viene allineato all&#39;interno della casella di testo utilizzando gli attributi di allineamento del testo rtf. Il testo può essere ritagliato dalla casella di testo.
1. Ridimensionare il contenuto di testo in base alla risoluzione specificata con `textAttr=`.
1. `rotate=`Applica , se specificato.
1. `extend=`Applica , se specificato.
1. Posizionate il livello nel quadro in base a `origin=` e `pos=`(vedete sotto).

Per entrambi i livelli immagine e testo, l&#39;ultimo passaggio, ovvero il posizionamento del livello nel quadro, non si applica al livello 0, poiché il livello 0 costituisce effettivamente il quadro.
