---
title: risolvere
description: Richiesta di debug. Questo comando di debug analizza ed elabora preventivamente la richiesta, esegue le ricerche nel catalogo delle immagini, include i modificatori di catalogo, sostituzioni di macro e variabili e così via, proprio come req=img.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
TQID: 'https://experienceleague.adobe.com/yS8k6Njz17UK9W42N6wyqmeg3FDweKnZ3vkMNw9wnJI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 0%

---

# risolvere{#resolve}

Richiesta di debug. Questo comando di debug analizza ed elabora preventivamente la richiesta, esegue le ricerche nel catalogo delle immagini, le inclusioni del catalogo::Modifier, le sostituzioni di macro e variabili e così via, proprio come req=img.

`req=resolve`

Viene restituita la stringa di richiesta finale, invece dell&#39;immagine risultante, con tipo MIME `text/plain`.

Risposta HTTP non memorizzabile in cache.
