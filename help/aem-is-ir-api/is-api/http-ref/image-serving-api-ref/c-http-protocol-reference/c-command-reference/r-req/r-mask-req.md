---
description: Maschera immagine. Richiede i dati della maschera (canale alfa).
solution: Experience Manager
title: maschera
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# maschera{#mask}

Maschera immagine. Richiede i dati della maschera (canale alfa).

`req=mask`

Supporta gli stessi comandi di `req=img`. Viene elaborato allo stesso modo dal server, ma invece di restituire i dati RGB o RGBA, il server elimina le informazioni sul colore e restituisce solo i dati maschera (canale alfa). Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`.

La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::Expiration`.
