---
description: Se req=img, la dimensione dell'area di lavoro di composizione è determinata interamente dalla dimensione del livello 0.
solution: Experience Manager
title: Area di lavoro di composizione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
TQID: 'https://experienceleague.adobe.com/62uvC05pApoYR5lY4A-KA5RHmW8Xz0r2-2yvOpdAkOo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# Area di lavoro di composizione{#the-compositing-canvas}

Se req=img, la dimensione dell&#39;area di lavoro di composizione è determinata interamente dalla dimensione del livello 0.

Se `size=` per il livello 0 non è specificato in modo esplicito, le trasformazioni di livello vengono utilizzate per calcolare le dimensioni dell&#39;area di lavoro di composizione (vedere di seguito).

Se `req=tmb`, la dimensione dell&#39;area di lavoro di composizione è determinata dal `size=` specificato per il livello 0 oppure, se non si specifica la dimensione, la dimensione dell&#39;area di lavoro di composizione è impostata sul rettangolo di visualizzazione (vedere di seguito).
