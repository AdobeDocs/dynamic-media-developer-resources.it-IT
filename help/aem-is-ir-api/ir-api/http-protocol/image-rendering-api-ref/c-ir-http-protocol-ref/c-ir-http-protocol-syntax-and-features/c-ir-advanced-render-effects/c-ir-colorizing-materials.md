---
title: Materiali coloranti
description: La maggior parte dei materiali può essere colorata dinamicamente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
TQID: 'https://experienceleague.adobe.com/MGmuOj214tFPKeSGwz33pGn2m0B0fme1Cq-umlxG9v0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# Materiali coloranti{#colorizing-materials}

La maggior parte dei materiali può essere colorata dinamicamente.

L&#39;algoritmo di colorizzazione è semplicistico e funziona meglio per le immagini di materiale con una gamma di tonalità limitata. Per colorare un materiale, il renderer sottrae semplicemente il valore `bgc=` e aggiunge il valore `color=` a ciascun valore di pixel.

La colorizzazione è disabilitata se `color=` non è specificato. L&#39;attributo `bgc=` viene ignorato dai materiali del cabinet. Viene utilizzato il valore del colore di base incorporato nel file [!DNL vnc].
