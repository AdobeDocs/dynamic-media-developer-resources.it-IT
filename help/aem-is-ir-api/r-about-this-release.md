---
description: Questa versione, Image Serving 6.6.1 e Image Rendering 6.6.1, sostituisce Image Serving 6.5.3 e Image Rendering 6.5.3.
seo-description: Questa versione, Image Serving 6.6.1 e Image Rendering 6.6.1, sostituisce Image Serving 6.5.3 e Image Rendering 6.5.3.
seo-title: Informazioni su questa versione
solution: Experience Manager
title: Informazioni su questa versione
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fdd8920-433b-405e-bf93-dbef5735be3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Informazioni su questa versione{#about-this-release}

Questa versione, Image Serving 6.6.1 e Image Rendering 6.6.1, sostituisce Image Serving 6.5.3 e Image Rendering 6.5.3.

## Problemi noti e modifiche di comportamento {#section-9dbc05206187477f926a78e8108a34e1}

* L’uso del carattere punto interrogativo negli ID risorsa non è più supportato, anche se il carattere è codificato nell’URL.
* Le richieste di banner dinamici `/xfl/flash/` non sono più supportate e ora restituiscono un codice di errore http 404.
* Le richieste W2P `/is/agm/` non sono più supportate.
* Alcuni messaggi di errore non vengono più visualizzati nel browser. Per eseguire il debug, è quindi necessario rivedere il registro di traccia.

## Nuove funzioni {#section-b1386e36cb4544ebb79766a06b16842d}

* Campione avanzato
* Ritaglio avanzato

## Correzione dei bug {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Problema risolto: l&#39;opzione RTF `\qc` seguita da uno spazio causava il mancato rendering di una richiesta.

