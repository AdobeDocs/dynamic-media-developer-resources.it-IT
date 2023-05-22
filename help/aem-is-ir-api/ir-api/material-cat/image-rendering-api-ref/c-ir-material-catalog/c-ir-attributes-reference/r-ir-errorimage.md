---
title: ErrorImage
description: Immagine di risposta di errore. In genere, il rendering immagini restituisce uno stato di errore con un messaggio di testo quando si verifica un errore.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---

# ErrorImage {#errorimage}

Immagine di risposta di errore. In genere, il rendering immagini restituisce uno stato di errore con un messaggio di testo quando si verifica un errore. Il `attribute::ErrorImage` consente di configurare un’immagine da restituire in caso di errore.

Quando si verifica un errore, il server tenta di interpretare il valore di `ImageRendering::attribute::ErrorImage`come semplice percorso del file di immagine. Se non è possibile aprire il file, invia il valore dell’attributo e i dettagli dell’errore a Image Server, che elabora come descritto in `ImageServing::attribute::ErrorImage`. Se Image Server non restituisce un’immagine di risposta valida, lo stato di errore HTTP standard e il messaggio di testo vengono inviati al client.

Le immagini di errore vengono restituite con lo stato HTTP 200.

## Proprietà {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Stringa di testo. Se specificato, deve essere un **`ImageServing::catalog::id`** valore, un percorso relativo (a **`ImageServing::attribute::RootPath`** o **`ImageRendering::attribute::RootPath`**) o un percorso assoluto di un file immagine accessibile dal server immagini.

## Predefinito {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Ereditato da `default::ErrorImage` se non è definita. Se è definita ma vuota, il comportamento dell’immagine di errore è disabilitato, anche se `default::ErrorImage` viene definito e viene restituito uno stato di errore HTTP.

## Consultate anche {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalogo::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
