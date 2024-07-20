---
title: Materiali coloranti
description: La maggior parte dei materiali può essere colorata dinamicamente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Materiali coloranti{#colorizing-materials}

La maggior parte dei materiali può essere colorata dinamicamente.

L&#39;algoritmo di colorizzazione è semplicistico e funziona meglio per le immagini di materiale con una gamma di tonalità limitata. Per colorare un materiale, il renderer sottrae semplicemente il valore `bgc=` e aggiunge il valore `color=` a ciascun valore di pixel.

La colorizzazione è disabilitata se `color=` non è specificato. L&#39;attributo `bgc=` viene ignorato dai materiali del cabinet. Viene utilizzato il valore del colore di base incorporato nel file [!DNL vnc].
