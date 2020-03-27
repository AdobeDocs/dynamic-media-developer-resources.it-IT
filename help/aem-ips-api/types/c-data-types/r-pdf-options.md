---
description: Opzioni del file PDF.
seo-description: Opzioni del file PDF.
seo-title: PDFOptions
solution: Experience Manager
title: PDFOptions
topic: Scene7 Image Production System API
uuid: 7558b6b5-ad32-4baf-896b-f4e2bd48f2ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PDFOptions{#pdfoptions}

Opzioni del file PDF.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`process`*` | `xsd:string` | Scelta dei &quot;processi PDF&quot;. |
| ` *`resolution`*` | `xsd:double` | Risoluzione del file. |
| ` *`colorspace`*` | `xsd:string` | Scelta della modalità spazio colore post-script. |
| ` *`pdfCatalog`*` | `xsd:boolean` | Se combinare un PDF con più pagine in un eCatalog dopo il rendering (impostazione predefinita: true). |
| ` *`extractSearchWords`*` | `xsd:boolean` | Se estrarre le parole di ricerca dal file PDF. |
| ` *`extractLinks`*` | `xsd:boolean` | Se estrarre i collegamenti PDF in mappe immagine assegnate alle pagine rasterizzate all’interno di IPS. |

