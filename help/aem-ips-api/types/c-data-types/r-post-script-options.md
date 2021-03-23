---
description: Opzioni del file PostScript.
seo-description: Opzioni del file PostScript.
seo-title: OpzioniPostScript
solution: Experience Manager
title: OpzioniPostScript
uuid: 31526bfe-b651-47a8-98c0-2750a3d9cabf
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 7%

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

