---
description: Opzioni del file PostScript.
solution: Experience Manager
title: OpzioniPostScript
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 8%

---


# PostScriptOptions{#postscriptoptions}

Opzioni del file PostScript.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`processo`*` | `xsd:string` | Selezione del processo PostScript. |
| `*`resolution`*` | `xsd:double` | Risoluzione del file. |
| `*`colorspace`*` | `xsd:string` | Modalità spazio colore PostScript. |
| `*`alfa`*` | `xsd:boolean` | Se rasterizzare il file in un’immagine. In tal caso, creerà uno sfondo trasparente se il file originale è definito in questo modo. Generalmente utilizzato per creare loghi sovrapposti. |
| `*`extractSearchWords`*` | `xsd:boolean` | Se estrarre le parole di ricerca dal file PostScript. |

