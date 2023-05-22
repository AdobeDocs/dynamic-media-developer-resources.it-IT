---
title: Posizionamento livello
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Posizionamento livello{#layer-placement}

I livelli vengono posizionati allineando l&#39;origine del livello (origine=) con l&#39;origine del livello di sfondo in corrispondenza di un offset specificato da pos=.

Se l&#39;origine del livello non è specificata in modo esplicito per un livello immagine, viene calcolata come segue:

1. Determinate l&#39;ancoraggio dell&#39;immagine. Utilizzare `anchor=`o, se non specificato, `catalog::Anchor`.
1. Se è definito l&#39;ancoraggio dell&#39;immagine, applicate le trasformazioni di livello e `extend=` per convertirlo in un valore origin=.
1. Se non è definito alcun ancoraggio immagine, l&#39;origine del livello viene posizionata al centro del rettangolo del livello (dopo l&#39;applicazione `extend=`).

![Immagine di posizionamento livello](assets/layerplacement.png)
