---
description: Opzioni del file PostScript.
solution: Experience Manager
title: Opzioni PostScript
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '65'
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
