---
description: Image Serving 6.6.1 e Image Rendering 6.6.1 sostituiscono Image Serving 6.5.3 e Image Rendering 6.5.3.
solution: Experience Manager
title: Informazioni su questa versione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Informazioni su questa versione{#about-this-release}

Image Serving 6.6.1 e Image Rendering 6.6.1 sostituiscono Image Serving 6.5.3 e Image Rendering 6.5.3.

## Problemi noti e modifiche del comportamento {#section-9dbc05206187477f926a78e8108a34e1}

* L’utilizzo del carattere del punto interrogativo negli ID risorsa non è più supportato, anche se il carattere è codificato in URL.
* Banner dinamico `/xfl/flash/` Le richieste non sono più supportate e ora restituiscono un codice di errore HTTP 404.
* W2P `/is/agm/` Le richieste di non sono più supportate.
* Alcuni messaggi di errore non vengono più visualizzati nel browser. Per eseguire il debug, è quindi necessario rivedere il registro di traccia.

## Nuove funzioni {#section-b1386e36cb4544ebb79766a06b16842d}

* Campione avanzato
* Ritaglio avanzato

## Correzione bug {#section-58dff74d56f64edeadf8f8b97b7a4161}

* È stato risolto un problema in cui `\qc` L’opzione RTF seguita da uno spazio ha impedito il rendering di una richiesta.
