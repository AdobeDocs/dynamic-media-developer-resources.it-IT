---
description: Opzioni del file PostScript.
solution: Experience Manager
title: Opzioni PostScript
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
TQID: 'https://experienceleague.adobe.com/XsIiYor0c-7I34OYazNaSF0Hx3sbZmzpTzAT1u73xxo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 4%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

Opzioni del file PostScript.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| processo | `xsd:string` | Scelta del processo PostScript. |
| risoluzione | `xsd:double` | Risoluzione dei file. |
| colorspace | `xsd:string` | modalità PostScript colorspace. |
| alfa | `xsd:boolean` | Specifica se rasterizzare il file in un&#39;immagine. In tal caso, viene creato uno sfondo trasparente se il file originale è definito in questo modo. Generalmente utilizzato per creare logo sovrapposti. |
| extractSearchWords | `xsd:boolean` | Indica se estrarre le parole di ricerca dal file PostScript. |
