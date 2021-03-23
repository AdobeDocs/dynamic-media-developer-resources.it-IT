---
description: Percorsi file di dati del catalogo del contenuto statico. Specifica i file che contengono i dati del contenuto statico per questo catalogo.
seo-description: Percorsi file di dati del catalogo del contenuto statico. Specifica i file che contengono i dati del contenuto statico per questo catalogo.
seo-title: FileCatalogoStatico
solution: Experience Manager
title: FileCatalogoStatico
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 3%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Percorsi file di dati del catalogo del contenuto statico. Specifica i file che contengono i dati del contenuto statico per questo catalogo.

I file di dati del catalogo del contenuto statico vengono caricati nell’ordine specificato. Se lo stesso valore `static::Id` si verifica in più record (nello stesso file di catalogo o in file di catalogo diversi), prevale l&#39;ultima istanza.

## Proprietà {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Uno o più valori di stringa di testo, separati da virgole. Facoltativo. Ogni valore deve essere un percorso o un percorso di file assoluto relativo alla cartella del catalogo.

## Predefinito {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vuoto, che indica che il catalogo immagini non include dati di contenuto statico.

## Consultate anche {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Dati del catalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
