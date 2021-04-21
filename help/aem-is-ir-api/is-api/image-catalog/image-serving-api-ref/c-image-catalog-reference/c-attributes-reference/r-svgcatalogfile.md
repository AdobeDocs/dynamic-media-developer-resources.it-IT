---
description: percorsi dei file di dati SVG. Specifica i file contenenti i dati SVG per questo catalogo.
solution: Experience Manager
title: FileCatalogoSvg
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# SvgCatalogFile{#svgcatalogfile}

percorsi dei file di dati SVG. Specifica i file contenenti i dati SVG per questo catalogo.

I file di dati SVG vengono caricati dopo tutti i file di dati immagine, nell&#39;ordine esatto specificato. Se lo stesso valore `catalog::Id` si verifica in più record (nella stessa immagine o in file di catalogo SVG diversi), prevale l&#39;ultima istanza.

## Proprietà {#section-fc2d549f76474792837b2b92ec2087ea}

Uno o più valori di stringa di testo, separati da virgole. Facoltativo. Ogni valore deve essere un percorso o un percorso di file assoluto relativo alla cartella del catalogo.

## Predefinito {#section-a4e58951f3c249599665b823566433c9}

Vuoto, che indica che questo catalogo immagini non include dati SVG.

## Consultate anche {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Dati](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29) catalogo,  [FileCatalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
