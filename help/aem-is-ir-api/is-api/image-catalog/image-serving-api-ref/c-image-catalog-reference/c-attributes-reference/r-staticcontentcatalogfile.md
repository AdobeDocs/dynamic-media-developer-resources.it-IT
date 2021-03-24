---
description: Percorsi file di dati del catalogo del contenuto statico. Specifica i file che contengono i dati del contenuto statico per questo catalogo.
solution: Experience Manager
title: FileCatalogoStatico
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

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
