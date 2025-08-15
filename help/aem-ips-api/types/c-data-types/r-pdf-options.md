---
description: Opzioni del file PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 4%

---

# [!DNL PDFOptions]{#pdfoptions}

Opzioni del file PDF.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| processo | `xsd:string` | Scelta di &quot;processi PDF&quot;. |
| risoluzione | `xsd:double` | Risoluzione dei file. |
| colorspace | `xsd:string` | Scelta modalità spazio colore post-script. |
| pdfCatalog | `xsd:boolean` | Specifica se combinare un PDF con più pagine in un eCatalog dopo il rendering (l&#39;impostazione predefinita è true). |
| extractSearchWords | `xsd:boolean` | Indica se estrarre le parole di ricerca dal file PDF. |
| extractLinks | `xsd:boolean` | Indica se estrarre i collegamenti PDF nelle mappe immagine assegnate alle pagine rasterizzate in IPS. |
