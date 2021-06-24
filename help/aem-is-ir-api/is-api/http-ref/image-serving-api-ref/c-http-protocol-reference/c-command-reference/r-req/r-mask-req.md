---
description: Maschera immagine. Richiede i dati della maschera (canale alfa).
solution: Experience Manager
title: maschera
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 12%

---

# maschera{#mask}

Maschera immagine. Richiede i dati della maschera (canale alfa).

`req=mask`

Supporta gli stessi comandi di `req=img`. Viene elaborato nello stesso modo dal server, ma invece di restituire i dati RGB o RGBA, il server scarta le informazioni sul colore e restituisce solo i dati della maschera (canale alfa). Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.
