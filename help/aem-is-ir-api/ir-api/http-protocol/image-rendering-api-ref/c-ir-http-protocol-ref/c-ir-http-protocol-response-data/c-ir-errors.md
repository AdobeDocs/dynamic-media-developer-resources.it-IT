---
title: Errori
description: Se una richiesta non può essere completata correttamente, il server restituisce un’immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
TQID: 'https://experienceleague.adobe.com/TSTpmfiuEppAPSUxX1ga5lfQSgWRkI2Wh1CXoalSU9A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# Errori{#errors}

Se una richiesta non può essere completata correttamente, il server restituisce un’immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.

Il valore dello stato della risposta dipende dal tipo di errore; per la maggior parte degli errori comuni, è &quot;403&quot;. Le risposte di errore per i tipi di richiesta non di immagine sono conformi al formato specificato con `req=`. (Al momento potrebbe non essere implementato in modo coerente.)

La quantità di dettagli inclusi nel messaggio di errore è configurabile con `attribute::ErrorDetail`.

**Immagini di errore**

Image Server può essere configurato per restituire i messaggi di errore di cui è stato eseguito il rendering in un’immagine. Per ulteriori dettagli, vedere `attribute::ErrorImage` nel catalogo immagini. Se l’immagine di errore viene generata correttamente, lo stato della risposta HTTP è 200. Se si verifica un errore durante l&#39;elaborazione dell&#39;immagine di errore, la risposta di errore HTTP standard e il messaggio di testo vengono restituiti al client.

**Vedere anche**

[attributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attributo::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
