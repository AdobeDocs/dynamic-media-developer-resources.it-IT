---
description: Se req=img, la dimensione dell'area di lavoro di composizione è determinata interamente dalla dimensione del livello 0.
solution: Experience Manager
title: Area di lavoro di composizione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Area di lavoro di composizione{#the-compositing-canvas}

Se req=img, la dimensione dell&#39;area di lavoro di composizione è determinata interamente dalla dimensione del livello 0.

Se `size=` per il livello 0 non è specificato in modo esplicito, le trasformazioni di livello vengono utilizzate per calcolare le dimensioni dell&#39;area di lavoro di composizione (vedere di seguito).

Se `req=tmb`, la dimensione dell&#39;area di lavoro di composizione è determinata dal `size=` specificato per il livello 0 oppure, se non si specifica la dimensione, la dimensione dell&#39;area di lavoro di composizione è impostata sul rettangolo di visualizzazione (vedere di seguito).
