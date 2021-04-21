---
description: Caricare la cache del server. Esegue la richiesta come req=img, ma invece di restituire l'immagine, il server restituisce la lunghezza dell'immagine di risposta (image.length), formattata come dati di testo con tipo MIME text/plain.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# loadcache{#loadcache}

Caricare la cache del server. Esegue la richiesta come req=img, ma invece di restituire l&#39;immagine, il server restituisce la lunghezza dell&#39;immagine di risposta (image.length), formattata come dati di testo con tipo MIME text/plain.

`req=loadcache`

La risposta HTTP non è memorizzabile nella cache.

Altri comandi nella richiesta si applicano come documentato.
