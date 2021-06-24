---
description: Cerca record stringa estratti da un file PDF.
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 9%

---

# SearchStrings{#searchstrings}

Cerca record stringa estratti da un file PDF.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`searchString`*` | `xsd:string` | Testo della stringa di ricerca. |
| `*`keywordsArray`*` | `types:KeywordsArray` | Array di parole chiave nella stringa di ricerca. |
| `*`status`*` | `xsd:boolean` | True se la stringa di ricerca è valida e abilitata. |
| `*`x`*` | `xsd:int` | Posizione dell&#39;asse X della stringa di ricerca. |
| `*`y`*` | `xsd:int` | Posizione dell&#39;asse Y della stringa di ricerca. |
| `*`width`*` | `xsd:int` | Larghezza stringa di ricerca. |
| `*`height`*` | `xsd:int` | Altezza stringa di ricerca. |
| `*`fontName`*` | `xsd:string` | Nome del font utilizzato nella stringa di ricerca. |
| `*`pointSize`*` | `xsd:string` | Dimensione del carattere. |
