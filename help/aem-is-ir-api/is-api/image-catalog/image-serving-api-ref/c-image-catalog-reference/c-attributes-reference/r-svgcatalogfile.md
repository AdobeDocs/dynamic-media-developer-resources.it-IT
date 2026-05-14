---
description: Percorsi dei file di dati di SVG. Specifica i file contenenti i dati SVG per questo catalogo.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 654579a2-33ff-4633-a6d0-3c03ec8d5aed
TQID: 'https://experienceleague.adobe.com/m1-nKj-KiVQlN70GYy1AFAAQN-M1wnxTGmmj-e3t9AY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 3%

---

# SvgCatalogFile{#svgcatalogfile}

Percorsi dei file di dati di SVG. Specifica i file contenenti i dati SVG per questo catalogo.

I file di dati SVG vengono caricati dopo tutti i file di dati immagine, nell’ordine esatto specificato. Se lo stesso valore `catalog::Id` si trova in più record (nella stessa immagine o in file di catalogo SVG), prevale l&#39;ultima istanza.

## Proprietà {#section-fc2d549f76474792837b2b92ec2087ea}

Uno o più valori stringa di testo separati da virgole. Facoltativo. Ogni valore deve essere un percorso assoluto o relativo alla cartella del catalogo.

## Predefinito {#section-a4e58951f3c249599665b823566433c9}

Vuoto: indica che questo catalogo immagini non include dati SVG.

## Consultate anche {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Dati catalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29), [FileCatalogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
