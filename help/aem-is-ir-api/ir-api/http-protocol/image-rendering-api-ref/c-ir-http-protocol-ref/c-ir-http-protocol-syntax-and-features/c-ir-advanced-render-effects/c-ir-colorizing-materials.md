---
description: La maggior parte dei materiali può essere colorata dinamicamente.
seo-description: La maggior parte dei materiali può essere colorata dinamicamente.
seo-title: Materiali coloranti
solution: Experience Manager
title: Materiali coloranti
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Colorazione di materiali{#colorizing-materials}

La maggior parte dei materiali può essere colorata dinamicamente.

L&#39;algoritmo di colorizzazione è molto semplice e funziona meglio per le immagini di materiale con una gamma di tonalità limitata. Per colorizzare un materiale, il renderer sottrae semplicemente il valore `bgc=` e aggiunge il valore `color=` a ciascun valore in pixel.

La colorazione è disabilitata se `color=` non è specificato. `bgc=` è ignorato dai materiali di armadio; viene invece utilizzato il valore del colore di base incorporato nel  [!DNL vnc] file.
