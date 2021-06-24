---
description: La maggior parte dei materiali può essere colorata dinamicamente.
solution: Experience Manager
title: Materiali coloranti
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Materiali coloranti{#colorizing-materials}

La maggior parte dei materiali può essere colorata dinamicamente.

L&#39;algoritmo di colorazione è abbastanza semplicistico e funziona meglio per le immagini di materiale con una gamma di tonalità limitata. Per colorare un materiale, il modulo di rendering sottrae semplicemente il valore `bgc=` e aggiunge il valore `color=` a ciascun valore di pixel.

La colorazione è disabilitata se `color=` non è specificato. `bgc=` è ignorato dai materiali dei cabinet; viene invece utilizzato il valore del colore di base incorporato nel  [!DNL vnc] file .
