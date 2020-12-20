---
description: Se req=img, la dimensione del quadro di composizione è determinata interamente dalla dimensione del livello 0.
seo-description: Se req=img, la dimensione del quadro di composizione è determinata interamente dalla dimensione del livello 0.
seo-title: Il quadro di composizione
solution: Experience Manager
title: Il quadro di composizione
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# Il quadro di composizione{#the-compositing-canvas}

Se req=img, la dimensione del quadro di composizione è determinata interamente dalla dimensione del livello 0.

Se il livello `size=` per il livello 0 non è specificato esplicitamente, le trasformazioni del livello vengono utilizzate per calcolare la dimensione del quadro di composizione (vedi sotto).

Se `req=tmb`, la dimensione del quadro di composizione è determinata dalla `size=` specificata per il livello 0, oppure, se la dimensione non è specificata, la dimensione del quadro di composizione è impostata sul recto della vista (vedi sotto).
