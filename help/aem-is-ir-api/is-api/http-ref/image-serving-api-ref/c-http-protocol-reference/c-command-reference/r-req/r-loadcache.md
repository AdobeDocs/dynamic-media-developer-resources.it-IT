---
description: Caricare la cache del server. Esegue la richiesta come req=img, ma invece di restituire l'immagine, il server restituisce la lunghezza dell'immagine di risposta (image.length), formattata come dati di testo con tipo MIME text/plain.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# loadcache{#loadcache}

Caricare la cache del server. Esegue la richiesta come req=img, ma invece di restituire l&#39;immagine, il server restituisce la lunghezza dell&#39;immagine di risposta (image.length), formattata come dati di testo con tipo MIME text/plain.

`req=loadcache`

La risposta HTTP non è memorizzabile nella cache.

Altri comandi nella richiesta si applicano come documentato.
