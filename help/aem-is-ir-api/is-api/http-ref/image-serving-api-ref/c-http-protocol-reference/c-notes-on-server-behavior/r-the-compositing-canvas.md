---
description: Se req=img, la dimensione del quadro di composizione è determinata interamente dalle dimensioni del livello 0.
seo-description: Se req=img, la dimensione del quadro di composizione è determinata interamente dalle dimensioni del livello 0.
seo-title: Il quadro di composizione
solution: Experience Manager
title: Il quadro di composizione
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Il quadro di composizione{#the-compositing-canvas}

Se req=img, la dimensione del quadro di composizione è determinata interamente dalle dimensioni del livello 0.

Se il `size=` per il livello 0 non è specificato esplicitamente, le trasformazioni del livello vengono utilizzate per calcolare le dimensioni dell&#39;area di composizione (vedi sotto).

Se `req=tmb`, la dimensione dell&#39;area di composizione è determinata dalla `size=` specificata per il livello 0 oppure, se non è specificata la dimensione, la dimensione dell&#39;area di composizione viene impostata sul campo di visualizzazione (vedi sotto).
