---
description: Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.
solution: Experience Manager
title: Trasformazioni livello
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5758d07c-bb84-4ab1-bf77-f59cf93f5e90
TQID: 'https://experienceleague.adobe.com/jChFcZzWWOlbicpu0WeRSJb608dGT9JmVSItV-uEjBY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 0%

---

# Trasformazioni livello{#layer-transforms}

Le trasformazioni vengono applicate alle immagini sorgente e ai livelli di testo.

Le seguenti operazioni vengono applicate alle immagini sorgente, nell&#39;ordine specificato, per ottenere la relazione spaziale desiderata con il livello 0:

1. Applica `crop=`, se specificato.
1. Ridimensionare in base a `size=` o, se `size=` non è specificato, in base a `scale=` oppure, se `scale=` non è specificato, in base a `res=` oppure, se `res=` non è specificato, utilizzare l&#39;immagine di origine a risoluzione completa.
1. Applica `flip=`, se specificato.
1. Applica `rotate=`, se specificato.
1. Applica `extend=`, se specificato.
1. Posizionare il livello nell&#39;area di lavoro in base a `origin=` e `pos=` (vedere di seguito).

Le seguenti trasformazioni vengono applicate ai livelli di testo:

1. La dimensione della casella di testo è determinata da `size=` oppure dalla larghezza e dall&#39;altezza del testo, se `size=` è specificato solo parzialmente o non è specificato affatto. Il testo viene allineato nella casella di testo utilizzando gli attributi di allineamento del testo rtf. Il testo può essere ritagliato dalla casella di testo.
1. Ridimensionare il contenuto di testo in base alla risoluzione specificata con `textAttr=`.
1. Applica `rotate=`, se specificato.
1. Applica `extend=`, se specificato.
1. Posizionare il livello nell&#39;area di lavoro in base a `origin=` e `pos=` (vedere di seguito).

Per entrambi i livelli immagine e testo, l’ultimo passaggio per posizionare il livello nell’area di lavoro non si applica al livello 0, poiché il livello 0 costituisce effettivamente l’area di lavoro.
