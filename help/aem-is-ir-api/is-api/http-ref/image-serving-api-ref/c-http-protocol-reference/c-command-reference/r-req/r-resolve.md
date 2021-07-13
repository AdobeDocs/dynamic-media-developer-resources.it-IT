---
description: Richiesta di debug. Questo comando di debug analizza e preelabora la richiesta, esegue ricerche di catalogo immagini, inclusioni modificatori di catalogo, sostituzioni di macro e variabili, ecc, proprio come req=img.
solution: Experience Manager
title: risolvere
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# risolvere{#resolve}

Richiesta di debug. Questo comando di debug analizza e preelabora la richiesta, esegue ricerche di catalogo immagini, catalogo::inclusioni modificatori, sostituzioni di macro e variabili, ecc, proprio come req=img.

`req=resolve`

Al posto dell’immagine del risultato, viene restituita la stringa di richiesta finale con il tipo MIME `text/plain`.

La risposta HTTP non è memorizzabile nella cache.
