---
description: Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.
solution: Experience Manager
title: Trasformazioni dei livelli
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---

# Trasformazioni dei livelli{#layer-transforms}

Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.

Le seguenti operazioni vengono applicate alle immagini sorgente, nell’ordine indicato, per ottenere la relazione spaziale desiderata con il livello 0:

1. Applicare `crop=`, se specificato.
1. Scala basata su `size=` o, se `size=` non è specificato, basata su `scale=` oppure, se `scale=` non è specificato, basata su `res=` o, se `res=`non è specificato, utilizza l&#39;immagine sorgente a risoluzione piena.
1. Applicare `flip=`, se specificato.
1. Applicare `rotate=`, se specificato.
1. Applicare `extend=`, se specificato.
1. Posiziona il livello nell’area di lavoro in base a `origin=` e `pos=` (vedi sotto).

Le seguenti trasformazioni vengono applicate ai livelli di testo:

1. Le dimensioni della casella di testo sono determinate da `size=`, oppure dalla larghezza e dall&#39;altezza del testo, se `size=` è fornito solo parzialmente o per nulla. Il testo viene allineato all’interno della casella di testo utilizzando gli attributi di allineamento del testo rtf. Il testo può essere ritagliato dalla casella di testo.
1. Ridimensiona il contenuto del testo in base alla risoluzione specificata con `textAttr=`.
1. Applicare `rotate=`, se specificato.
1. Applicare `extend=`, se specificato.
1. Posiziona il livello nell’area di lavoro in base a `origin=` e `pos=` (vedi sotto).

Per i livelli immagine e testo, l’ultimo passaggio di posizionamento del livello nell’area di lavoro non si applica al livello 0, poiché il livello 0 costituisce effettivamente l’area di lavoro.
