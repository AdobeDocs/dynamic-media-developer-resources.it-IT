---
description: Maschera immagine. Richiede i dati della maschera (canale alfa).
seo-description: Maschera immagine. Richiede i dati della maschera (canale alfa).
seo-title: mask
solution: Experience Manager
title: mask
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 11%

---


# mask{#mask}

Maschera immagine. Richiede i dati della maschera (canale alfa).

`req=mask`

Supporta gli stessi comandi di `req=img` ed è elaborato allo stesso modo dal server, ma invece di restituire i dati RGB o RGBA, il server scarta le informazioni sul colore e restituisce solo i dati della maschera (canale alfa). Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.
