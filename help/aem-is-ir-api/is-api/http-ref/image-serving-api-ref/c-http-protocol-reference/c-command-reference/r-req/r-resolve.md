---
description: Richiesta di debug. Questo comando di debug analizza ed elabora preventivamente la richiesta, esegue le ricerche nel catalogo delle immagini, include i modificatori di catalogo, sostituzioni di macro e variabili e così via, proprio come req=img.
solution: Experience Manager
title: risolvere
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# risolvere{#resolve}

Richiesta di debug. Questo comando di debug analizza ed elabora preventivamente la richiesta, esegue le ricerche nel catalogo delle immagini, le inclusioni del catalogo::Modifier, le sostituzioni di macro e variabili e così via, proprio come req=img.

`req=resolve`

Viene restituita la stringa di richiesta finale, invece dell’immagine risultante, con tipo MIME `text/plain`.

Risposta HTTP non memorizzabile in cache.
