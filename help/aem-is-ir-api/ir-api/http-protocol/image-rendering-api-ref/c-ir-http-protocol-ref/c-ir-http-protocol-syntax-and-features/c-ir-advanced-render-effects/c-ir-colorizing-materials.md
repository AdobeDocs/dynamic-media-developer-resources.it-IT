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

L&#39;algoritmo di colorizzazione è semplicistico e funziona meglio per le immagini di materiale con una gamma di tonalità limitata. Per colorare un materiale, il renderer sottrae semplicemente il `bgc=` e aggiunge `color=` valore per ciascun valore pixel.

La colorazione è disattivata se `color=` non è specificato. Il `bgc=` l&#39;attributo viene ignorato dai materiali dell&#39;archivio; il valore del colore di base è incorporato nel [!DNL vnc] al suo posto viene utilizzato il file.
