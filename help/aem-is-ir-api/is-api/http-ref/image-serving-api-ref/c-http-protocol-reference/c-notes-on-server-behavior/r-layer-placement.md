---
description: I livelli vengono posizionati allineando l’origine del livello (origin=) con l’origine del livello di sfondo a un offset specificato da pos=.
seo-description: I livelli vengono posizionati allineando l’origine del livello (origin=) con l’origine del livello di sfondo a un offset specificato da pos=.
seo-title: Posizionamento del livello
solution: Experience Manager
title: Posizionamento del livello
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Posizionamento del livello{#layer-placement}

I livelli vengono posizionati allineando l’origine del livello (origin=) con l’origine del livello di sfondo a un offset specificato da pos=.

Se l’origine del livello non è specificata esplicitamente per un livello immagine, viene calcolata come segue:

1. Consente di definire l’ancoraggio dell’immagine. Utilizzare `anchor=`, o, se non specificato, `catalog::Anchor`.
1. Se l’ancoraggio immagine è definito, applicate le trasformazioni del livello e `extend=` convertirlo in un valore origin=.
1. Se non è definito alcun ancoraggio immagine, l’origine del livello viene posizionata al centro del rettangolo del livello (dopo l’applicazione `extend=`).

![](assets/layerplacement.png)

