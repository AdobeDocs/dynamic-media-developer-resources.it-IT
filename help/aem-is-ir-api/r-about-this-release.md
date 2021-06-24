---
description: Questa versione (Image Serving 6.6.1 e Image Rendering 6.6.1) sostituisce Image Serving 6.5.3 e Image Rendering 6.5.3.
solution: Experience Manager
title: Informazioni su questa versione
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Informazioni su questa versione{#about-this-release}

Questa versione (Image Serving 6.6.1 e Image Rendering 6.6.1) sostituisce Image Serving 6.5.3 e Image Rendering 6.5.3.

## Problemi noti e modifiche al comportamento {#section-9dbc05206187477f926a78e8108a34e1}

* L’uso del carattere del punto interrogativo negli ID delle risorse non è più supportato, anche se il carattere è codificato nell’URL.
* Le richieste di banner dinamici `/xfl/flash/` non sono più supportate e ora restituiscono un codice di errore http 404.
* Le richieste W2P `/is/agm/` non sono più supportate.
* Alcuni messaggi di errore non vengono più visualizzati nel browser. Per eseguire il debug, è quindi necessario rivedere il registro di traccia.

## Nuove funzioni {#section-b1386e36cb4544ebb79766a06b16842d}

* Campione avanzato
* Ritaglio avanzato

## Correzione bug {#section-58dff74d56f64edeadf8f8b97b7a4161}

* È stato risolto un problema a causa del quale l&#39;opzione `\qc` RTF seguita da uno spazio impediva il rendering di una richiesta.
