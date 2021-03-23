---
description: I livelli vengono posizionati allineando l'origine del livello (origin=) con l'origine del livello di sfondo a un offset specificato da pos=.
seo-description: I livelli vengono posizionati allineando l'origine del livello (origin=) con l'origine del livello di sfondo a un offset specificato da pos=.
seo-title: Posizionamento livello
solution: Experience Manager
title: Posizionamento livello
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Posizionamento livello{#layer-placement}

I livelli vengono posizionati allineando l&#39;origine del livello (origin=) con l&#39;origine del livello di sfondo a un offset specificato da pos=.

Se l’origine del livello non è specificata esplicitamente per un livello immagine, viene calcolata come segue:

1. Determinare l’ancoraggio dell’immagine. Utilizzare `anchor=` o, se non specificato, `catalog::Anchor`.
1. Se è definito l’ancoraggio dell’immagine, applica le trasformazioni di livello e `extend=` per convertirlo in un valore origin= .
1. Se non è definito alcun ancoraggio immagine, l’origine del livello viene posizionata al centro del rettangolo del livello (dopo l’applicazione di `extend=`).

![](assets/layerplacement.png)

