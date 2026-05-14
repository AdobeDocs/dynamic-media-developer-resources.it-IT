---
description: Maschera immagine. Richiede i dati della maschera (canale alfa).
solution: Experience Manager
title: maschera
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
TQID: 'https://experienceleague.adobe.com/FMsQMZsc3N1ToEzXBE0vOzkezfemSzT6NaGJQ1gQqd8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# maschera{#mask}

Maschera immagine. Richiede i dati della maschera (canale alfa).

`req=mask`

Supporta gli stessi comandi di `req=img`. Viene elaborato allo stesso modo dal server, ma invece di restituire i dati RGB o RGBA, il server elimina le informazioni sul colore e restituisce solo i dati della maschera (canale alfa). Il formato dei dati di risposta e il tipo MIME di risposta sono determinati da `fmt=`.

La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::Expiration`.
