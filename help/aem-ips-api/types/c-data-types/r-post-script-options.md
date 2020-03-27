---
description: Opzioni del file PostScript.
seo-description: Opzioni del file PostScript.
seo-title: PostScriptOptions
solution: Experience Manager
title: PostScriptOptions
topic: Scene7 Image Production System API
uuid: 31526bfe-b651-47a8-98c0-2750a3d9cabf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostScriptOptions{#postscriptoptions}

Opzioni del file PostScript.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`process`*` | `xsd:string` | PostScript process choice. |
| ` *`resolution`*` | `xsd:double` | Risoluzione del file. |
| ` *`colorspace`*` | `xsd:string` | Modalità spazio colore PostScript. |
| ` *`alfa`*` | `xsd:boolean` | Se rasterizzare il file in un’immagine. In tal caso, se il file originale è definito in questo modo, verrà creato uno sfondo trasparente. Generalmente utilizzato per creare logo sovrapposti. |
| ` *`extractSearchWords`*` | `xsd:boolean` | Se estrarre le parole di ricerca dal file PostScript. |

