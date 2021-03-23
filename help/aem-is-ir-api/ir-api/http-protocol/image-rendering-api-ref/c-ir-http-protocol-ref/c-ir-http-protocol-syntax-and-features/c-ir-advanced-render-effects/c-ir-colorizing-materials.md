---
description: La maggior parte dei materiali può essere colorata dinamicamente.
seo-description: La maggior parte dei materiali può essere colorata dinamicamente.
seo-title: Materiali coloranti
solution: Experience Manager
title: Materiali coloranti
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# Materiali di colorazione{#colorizing-materials}

La maggior parte dei materiali può essere colorata dinamicamente.

L&#39;algoritmo di colorazione è abbastanza semplicistico e funziona meglio per le immagini di materiale con una gamma di tonalità limitata. Per colorare un materiale, il modulo di rendering sottrae semplicemente il valore `bgc=` e aggiunge il valore `color=` a ciascun valore di pixel.

La colorazione è disabilitata se `color=` non è specificato. `bgc=` è ignorato dai materiali dei cabinet; viene invece utilizzato il valore del colore di base incorporato nel  [!DNL vnc] file .
