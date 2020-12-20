---
description: Durata predefinita cache client. Fornisce un intervallo di scadenza predefinito nel caso in cui un determinato record di catalogo non contenga un valore valido per la scadenza del catalogo o della vignettatura, oppure se l'accesso a un file di vignettatura o materiale è diretto, anziché tramite un record di catalogo.
seo-description: Durata predefinita cache client. Fornisce un intervallo di scadenza predefinito nel caso in cui un determinato record di catalogo non contenga un valore valido per la scadenza del catalogo o della vignettatura, oppure se l'accesso a un file di vignettatura o materiale è diretto, anziché tramite un record di catalogo.
seo-title: Scadenza
solution: Experience Manager
title: Scadenza
topic: Scene7 Image Serving - Image Rendering API
uuid: 2b56f9ec-2b25-4e6a-aead-6dad3d2df975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# Scadenza{#expiration}

Durata predefinita cache client. Fornisce un intervallo di scadenza predefinito nel caso in cui un determinato record di catalogo non contenga un catalogo valido::Scadenza o vignettatura::Scadenza, oppure se un file di vignettatura o di materiale è accessibile direttamente, anziché tramite un record di catalogo.

## Proprietà {#section-8e2bade105ec4905ae5c4911f500279f}

Numero reale, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dei dati di risposta. Impostate su 0 per scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Impostare su -1 per contrassegnare come *non scade mai*.

## Predefinito {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Ereditato da default::Expiration se non definito o se vuoto.

## Consultate anche {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalogo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [vignettatura::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
