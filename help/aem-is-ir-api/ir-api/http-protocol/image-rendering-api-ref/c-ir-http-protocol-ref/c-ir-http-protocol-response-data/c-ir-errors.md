---
description: Se una richiesta non può essere completata correttamente, il server restituirà un’immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.
seo-description: Se una richiesta non può essere completata correttamente, il server restituirà un’immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.
seo-title: Errori
solution: Experience Manager
title: Errori
topic: Scene7 Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---


# Errori{#errors}

Se una richiesta non può essere completata correttamente, il server restituirà un’immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.

Il valore dello stato della risposta dipende dal tipo di errore; per la maggior parte degli errori più comuni è &#39;403&#39;. Le risposte di errore per i tipi di richieste non di immagini sono conformi al formato specificato con `req=`. (Al momento potrebbe non essere implementata in modo coerente).

La quantità di dettagli inclusa nel messaggio di errore è configurabile con `attribute::ErrorDetail`.

**Immagini di errore**

Image Server può essere configurato per restituire i messaggi di errore sottoposti a rendering in un’immagine. Per informazioni, consultate `attribute::ErrorImage` nel riferimento al catalogo immagini. Se l&#39;immagine di errore viene generata correttamente, lo stato della risposta HTTP è 200. Se si verifica un errore durante l&#39;elaborazione dell&#39;immagine di errore, la risposta di errore HTTP standard e il messaggio di testo vengono restituiti al client.

**Consultate anche**

[attributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attributo::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
