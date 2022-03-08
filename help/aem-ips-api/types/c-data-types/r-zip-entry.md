---
description: Una voce in un file ZIP.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 11%

---

# ZipEntry{#zipentry}

Una voce in un file ZIP.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| name | `xsd:string` | Nome della voce. |
| isDirectory | `xsd:boolean` | Determina se la voce è una directory. |
| lastModified | `xsd:dateTime` | Data e ora dell’ultima modifica. |
| compressedSize | `xsd:long` | Dimensione compressa. |
| uncompressedSize | `xsd:long` | Dimensione non compressa. |
