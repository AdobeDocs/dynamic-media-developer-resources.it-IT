---
description: La maggior parte dei materiali può essere colorata dinamicamente.
solution: Experience Manager
title: Materiali coloranti
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Materiali di colorazione{#colorizing-materials}

La maggior parte dei materiali può essere colorata dinamicamente.

L&#39;algoritmo di colorazione è abbastanza semplicistico e funziona meglio per le immagini di materiale con una gamma di tonalità limitata. Per colorare un materiale, il modulo di rendering sottrae semplicemente il valore `bgc=` e aggiunge il valore `color=` a ciascun valore di pixel.

La colorazione è disabilitata se `color=` non è specificato. `bgc=` è ignorato dai materiali dei cabinet; viene invece utilizzato il valore del colore di base incorporato nel  [!DNL vnc] file .
