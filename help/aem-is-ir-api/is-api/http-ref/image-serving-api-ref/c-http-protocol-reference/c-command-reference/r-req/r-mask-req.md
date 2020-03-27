---
description: Maschera immagine. Richiede i dati della maschera (canale alfa).
seo-description: Maschera immagine. Richiede i dati della maschera (canale alfa).
seo-title: mask
solution: Experience Manager
title: mask
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mask{#mask}

Maschera immagine. Richiede i dati della maschera (canale alfa).

`req=mask`

Supporta gli stessi comandi `req=img`e viene elaborato allo stesso modo dal server, ma invece di restituire i dati RGB o RGBA, il server scarta le informazioni sui colori e restituisce solo i dati della maschera (canale alfa). Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.
