---
description: Percorsi dei file di dati delle immagini. Specifica i file che contengono i dati immagine per questo catalogo.
solution: Experience Manager
title: FileCatalogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 3%

---

# FileCatalogo{#catalogfile}

Percorsi dei file di dati delle immagini. Specifica i file che contengono i dati immagine per questo catalogo.

I file di dati immagine vengono caricati nell&#39;ordine specificato. Se lo stesso `catalog::Id` si trova in più record (nello stesso file di catalogo o in file di catalogo diversi), l&#39;ultima istanza prevale.

## Proprietà {#section-6da55f145ecd4e31a5de52637a436983}

Uno o più valori stringa di testo separati da virgole. Facoltativo. Ogni valore deve essere un percorso assoluto o relativo alla cartella del catalogo.

## Predefinito {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vuoto: indica che questo catalogo immagini non include dati immagine.

## Consultate anche {#section-910b67c5041d44d99a105ad43ff63a37}

[Campi dati catalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
