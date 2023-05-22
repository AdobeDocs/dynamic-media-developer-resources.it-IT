---
description: Opzioni del file PostScript.
solution: Experience Manager
title: Opzioni PostScript
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 6%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

Opzioni del file PostScript.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| processo | `xsd:string` | Scelta del processo PostScript. |
| risoluzione | `xsd:double` | Risoluzione dei file. |
| colorspace | `xsd:string` | Modalità spazio colore PostScript. |
| alfa | `xsd:boolean` | Specifica se rasterizzare il file in un&#39;immagine. In tal caso, se il file originale è definito in questo modo, verrà creato uno sfondo trasparente. Generalmente utilizzato per creare logo sovrapposti. |
| extractSearchWords | `xsd:boolean` | Indica se estrarre le parole di ricerca dal file PostScript. |
