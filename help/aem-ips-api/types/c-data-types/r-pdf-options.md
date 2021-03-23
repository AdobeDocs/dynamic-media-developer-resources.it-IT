---
description: Opzioni del file PDF.
seo-description: Opzioni del file PDF.
seo-title: PDFOptions
solution: Experience Manager
title: PDFOptions
uuid: 7558b6b5-ad32-4baf-896b-f4e2bd48f2ec
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---


# PDFOptions{#pdfoptions}

Opzioni del file PDF.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`processo`*` | `xsd:string` | Scelta dei &quot;processi PDF&quot;. |
| `*`resolution`*` | `xsd:double` | Risoluzione del file. |
| `*`colorspace`*` | `xsd:string` | Scelta della modalità a colori post-script. |
| `*`pdfCatalog`*` | `xsd:boolean` | Se combinare un PDF a più pagine in un eCatalog dopo il rendering (l’impostazione predefinita è true). |
| `*`extractSearchWords`*` | `xsd:boolean` | Se estrarre parole di ricerca dal file PDF. |
| `*`extractLinks`*` | `xsd:boolean` | Se estrarre collegamenti PDF in mappe immagine assegnate alle pagine rasterizzate all’interno di IPS. |

