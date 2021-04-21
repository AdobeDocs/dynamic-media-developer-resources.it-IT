---
description: Maschera immagine. Richiede i dati della maschera (canale alfa).
solution: Experience Manager
title: maschera
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 11%

---


# mask{#mask}

Maschera immagine. Richiede i dati della maschera (canale alfa).

`req=mask`

Supporta gli stessi comandi di `req=img`. Viene elaborato nello stesso modo dal server, ma invece di restituire i dati RGB o RGBA, il server scarta le informazioni sul colore e restituisce solo i dati della maschera (canale alfa). Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.
