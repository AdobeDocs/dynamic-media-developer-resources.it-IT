---
description: Percorsi dei file di dati SVG. Specifica i file contenenti i dati SVG per questo catalogo.
seo-description: Percorsi dei file di dati SVG. Specifica i file contenenti i dati SVG per questo catalogo.
seo-title: SvgCatalogFile
solution: Experience Manager
title: SvgCatalogFile
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f0c8e687-77cc-4ca7-b2c2-6ba8960e11e6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# SvgCatalogFile{#svgcatalogfile}

Percorsi dei file di dati SVG. Specifica i file contenenti i dati SVG per questo catalogo.

I file di dati SVG vengono caricati dopo tutti i file di dati immagine, nell&#39;ordine esatto specificato. Se lo stesso valore `catalog::Id` si verifica in più record (nella stessa immagine o in file di catalogo SVG diversi), prevale l&#39;ultima istanza.

## Proprietà {#section-fc2d549f76474792837b2b92ec2087ea}

Uno o più valori stringa di testo, separati da virgole. Facoltativo. Ogni valore deve essere un percorso o un percorso di file assoluto relativo alla cartella del catalogo.

## Predefinito {#section-a4e58951f3c249599665b823566433c9}

Vuoto, che indica che questo catalogo immagini non include dati SVG.

## Consultate anche {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Dati](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29) catalogo,  [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
