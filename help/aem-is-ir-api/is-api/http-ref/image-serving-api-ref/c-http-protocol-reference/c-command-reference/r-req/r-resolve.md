---
description: Richiesta di debug. Questo comando di debug analizza e preelabora la richiesta, esegue ricerche di catalogo immagini, inclusioni modificatori di catalogo, sostituzioni di macro e variabili, ecc, proprio come req=img.
solution: Experience Manager
title: risolvere
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# risolvere{#resolve}

Richiesta di debug. Questo comando di debug analizza e preelabora la richiesta, esegue ricerche di catalogo immagini, catalogo::inclusioni modificatori, sostituzioni di macro e variabili, ecc, proprio come req=img.

`req=resolve`

Al posto dell’immagine del risultato, viene restituita la stringa di richiesta finale con il tipo MIME `text/plain`.

La risposta HTTP non è memorizzabile nella cache.
