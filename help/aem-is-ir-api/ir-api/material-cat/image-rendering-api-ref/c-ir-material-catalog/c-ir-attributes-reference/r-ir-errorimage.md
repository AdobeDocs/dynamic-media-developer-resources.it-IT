---
description: Immagine della risposta di errore. In genere, il rendering delle immagini restituisce uno stato di errore con un messaggio di testo quando si verifica un errore. attribute ErrorImage consente la configurazione di un'immagine da restituire in caso di errore.
seo-description: Immagine della risposta di errore. In genere, il rendering delle immagini restituisce uno stato di errore con un messaggio di testo quando si verifica un errore. attribute ErrorImage consente la configurazione di un'immagine da restituire in caso di errore.
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# ErrorImage *{#errorimage}

Immagine della risposta di errore. In genere, il rendering delle immagini restituisce uno stato di errore con un messaggio di testo quando si verifica un errore. attribute::ErrorImage consente la configurazione di un&#39;immagine da restituire in caso di errore.

Quando si verifica un errore, il server tenta innanzitutto di interpretare il valore di `ImageRendering::attribute::ErrorImage`come un semplice percorso del file di immagine. Se il file non può essere aperto, invia il valore dell&#39;attributo e i dettagli dell&#39;errore a Image Server, che elabora come descritto in `ImageServing::attribute::ErrorImage`. Se Image Server non restituisce un&#39;immagine di risposta valida, lo stato di errore HTTP standard e il messaggio di testo vengono inviati al client.

Le immagini di errore vengono restituite con lo stato HTTP 200.

## Proprietà {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Stringa di testo. Se specificato, deve essere un valore **`ImageServing::catalog::id`**, un percorso relativo (a **`ImageServing::attribute::RootPath`** o **`ImageRendering::attribute::RootPath`**) oppure un percorso assoluto di un file di immagine accessibile dal server immagini.

## Predefinito {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Ereditato da `default::ErrorImage` se non è definito. Se è definito ma vuoto, il comportamento dell&#39;immagine di errore è disabilitato, anche se è definito `default::ErrorImage`, e viene restituito uno stato di errore HTTP.

## Consultate anche {#section-3e0308eaf4124451909dacd570e27695}

[attributo::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalogo::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
