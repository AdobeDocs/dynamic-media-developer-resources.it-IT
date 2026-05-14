---
description: Record di stringa di ricerca estratto da un file PDF.
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
TQID: 'https://experienceleague.adobe.com/bWokSVoIEkxrKgXAkaR4ycgSjZAWb2trFnqokTe98XQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# [!DNL SearchStrings]{#searchstrings}

Record di stringa di ricerca estratto da un file PDF.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| searchString | `xsd:string` | Testo stringa di ricerca. |
| keywordsArray | `types:KeywordsArray` | Array di parole chiave nella stringa di ricerca. |
| stato | `xsd:boolean` | True se la stringa di ricerca è valida e abilitata. |
| x | `xsd:int` | Posizione asse X della stringa di ricerca. |
| y | `xsd:int` | Posizione asse Y della stringa di ricerca. |
| larghezza | `xsd:int` | Larghezza stringa di ricerca. |
| altezza | `xsd:int` | Altezza stringa di ricerca. |
| fontName | `xsd:string` | Nome del font utilizzato nella stringa di ricerca. |
| pointSize | `xsd:string` | Dimensione font. |
