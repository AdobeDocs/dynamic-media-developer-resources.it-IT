---
description: Se req=img, la dimensione del quadro di composizione è determinata interamente dalle dimensioni del livello 0.
solution: Experience Manager
title: Il quadro di composizione
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# Il quadro di composizione{#the-compositing-canvas}

Se req=img, la dimensione del quadro di composizione è determinata interamente dalle dimensioni del livello 0.

Se il `size=` per il livello 0 non è specificato esplicitamente, le trasformazioni del livello vengono utilizzate per calcolare le dimensioni dell&#39;area di composizione (vedi sotto).

Se `req=tmb`, la dimensione dell&#39;area di composizione è determinata dalla `size=` specificata per il livello 0 oppure, se non è specificata la dimensione, la dimensione dell&#39;area di composizione viene impostata sul campo di visualizzazione (vedi sotto).
