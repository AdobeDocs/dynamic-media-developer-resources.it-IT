---
description: Precaricare la cache del server. Esegue la richiesta esattamente come req=img, ma invece di restituire l'immagine, il server restituisce la lunghezza dell'immagine di risposta (image.length), formattata come dati di testo con tipo MIME text/plain.
seo-description: Precaricare la cache del server. Esegue la richiesta esattamente come req=img, ma invece di restituire l'immagine, il server restituisce la lunghezza dell'immagine di risposta (image.length), formattata come dati di testo con tipo MIME text/plain.
seo-title: loadcache
solution: Experience Manager
title: loadcache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 44f0db05-2323-4aa2-853c-f78e656a4308
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# loadcache{#loadcache}

Precaricare la cache del server. Esegue la richiesta esattamente come req=img, ma invece di restituire l&#39;immagine, il server restituisce la lunghezza dell&#39;immagine di risposta (image.length), formattata come dati di testo con tipo MIME text/plain.

`req=loadcache`

La risposta HTTP non è memorizzabile nella cache.

Gli altri comandi nella richiesta si applicano come documentato.
