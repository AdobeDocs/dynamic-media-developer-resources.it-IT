---
description: Se una richiesta non può essere completata correttamente, il server restituisce un’immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.
solution: Experience Manager
title: Errori
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Errori{#errors}

Se una richiesta non può essere completata correttamente, il server restituisce un’immagine di errore o uno stato di risposta HTTP diverso da 200 insieme a un messaggio di errore.

Il valore dello stato della risposta dipende dal tipo di errore; per la maggior parte degli errori comuni è &quot;403&quot;. Le risposte di errore per i tipi di richiesta non di immagine sono conformi al formato specificato con `req=`. (Al momento potrebbe non essere implementato in modo coerente).

La quantità di dettagli inclusi nel messaggio di errore è configurabile con `attribute::ErrorDetail`.

## Immagini di errore {#section-92e9b20b2507433daa96923abc95f777}

Image Server può essere configurato per restituire i messaggi di errore di cui è stato eseguito il rendering in un’immagine.

Per ulteriori informazioni, vedere [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) nel riferimento al catalogo immagini.

Se l’immagine di errore viene generata correttamente, lo stato della risposta HTTP è 200. Se si verifica un errore durante l&#39;elaborazione dell&#39;immagine di errore, la risposta di errore HTTP standard e il messaggio di testo vengono restituiti al client.

## Immagine predefinita {#section-66bf25fe6b434081bfae96d38d9be25e}

Image Server può essere configurato in modo da sostituire un’immagine mancante con un’immagine predefinita. L&#39;immagine predefinita può essere specificata con `attribute::DefaultImage` o con il comando `defaultImage=`.

## Consultate anche {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
