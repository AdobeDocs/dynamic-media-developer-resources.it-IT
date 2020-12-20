---
description: Percorsi dei file di dati immagine. Specifica i file che contengono i dati immagine per questo catalogo.
seo-description: Percorsi dei file di dati immagine. Specifica i file che contengono i dati immagine per questo catalogo.
seo-title: CatalogFile
solution: Experience Manager
title: CatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 3599c8d3-dc4b-434e-8b11-775ea6f155ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# CatalogFile{#catalogfile}

Percorsi dei file di dati immagine. Specifica i file che contengono i dati immagine per questo catalogo.

I file di dati immagine vengono caricati nell&#39;ordine specificato. Se lo stesso valore `catalog::Id` si verifica in più record (nello stesso o in file di catalogo diversi), prevale l&#39;ultima istanza.

## Proprietà {#section-6da55f145ecd4e31a5de52637a436983}

Uno o più valori stringa di testo, separati da virgole. Facoltativo. Ogni valore deve essere un percorso o un percorso di file assoluto relativo alla cartella del catalogo.

## Predefinito {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vuoto, che indica che questo catalogo immagini non include dati immagine.

## Consultate anche {#section-910b67c5041d44d99a105ad43ff63a37}

[Campi dati catalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
