---
description: Opzioni del file PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '73'
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
