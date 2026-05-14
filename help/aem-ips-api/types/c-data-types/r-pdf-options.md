---
description: Opzioni del file PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
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
