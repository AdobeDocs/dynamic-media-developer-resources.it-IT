---
description: Percorsi del file di dati del catalogo del contenuto statico. Specifica i file che contengono i dati del contenuto statico per il catalogo.
seo-description: Percorsi del file di dati del catalogo del contenuto statico. Specifica i file che contengono i dati del contenuto statico per il catalogo.
seo-title: StaticContentCatalogFile
solution: Experience Manager
title: StaticContentCatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 3%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Percorsi del file di dati del catalogo del contenuto statico. Specifica i file che contengono i dati del contenuto statico per il catalogo.

I file di dati del catalogo del contenuto statico vengono caricati nell&#39;ordine specificato. Se lo stesso valore `static::Id` si verifica in più record (nello stesso o in file di catalogo diversi), prevale l&#39;ultima istanza.

## Proprietà {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Uno o più valori stringa di testo, separati da virgole. Facoltativo. Ogni valore deve essere un percorso o un percorso di file assoluto relativo alla cartella del catalogo.

## Predefinito {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vuoto, che indica che questo catalogo immagini non include dati di contenuto statici.

## Consultate anche {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Dati catalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
