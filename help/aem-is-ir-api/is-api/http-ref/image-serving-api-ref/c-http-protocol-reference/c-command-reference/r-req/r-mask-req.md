---
description: Maschera immagine. Richiede i dati della maschera (canale alfa).
seo-description: Maschera immagine. Richiede i dati della maschera (canale alfa).
seo-title: maschera
solution: Experience Manager
title: maschera
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

---


# mask{#mask}

Maschera immagine. Richiede i dati della maschera (canale alfa).

`req=mask`

Supporta gli stessi comandi di `req=img` e viene elaborato nello stesso modo dal server, ma invece di restituire i dati RGB o RGBA, il server elimina le informazioni sul colore e restituisce solo i dati della maschera (canale alfa). Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.
