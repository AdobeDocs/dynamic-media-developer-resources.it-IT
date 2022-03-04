---
title: Errori
description: Se una richiesta non può essere completata correttamente, il server restituisce un'immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---

# Errori{#errors}

Se una richiesta non può essere completata correttamente, il server restituisce un&#39;immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.

Il valore dello stato della risposta dipende dal tipo di errore; per la maggior parte degli errori comuni, è &#39;403&#39;. Le risposte di errore per i tipi di richiesta non immagine sono conformi al formato specificato con `req=`. (Al momento potrebbe non essere implementato in modo coerente).

La quantità di dettagli inclusi nel messaggio di errore è configurabile con `attribute::ErrorDetail`.

**Immagini di errore**

Image Server può essere configurato per restituire i messaggi di errore sottoposti a rendering in un&#39;immagine. Vedi `attribute::ErrorImage` per ulteriori informazioni, vedere il riferimento al catalogo delle immagini. Se l’immagine di errore viene generata correttamente, lo stato della risposta HTTP è 200. Se si verifica un errore durante l’elaborazione dell’immagine di errore, la risposta di errore HTTP standard e il messaggio di testo vengono restituiti al client.

**Consultate anche**

[attributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attributo::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
