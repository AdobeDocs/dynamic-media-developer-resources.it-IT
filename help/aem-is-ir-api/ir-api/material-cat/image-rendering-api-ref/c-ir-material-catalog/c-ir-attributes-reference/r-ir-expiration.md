---
description: Tempo predefinito della cache del client per la durata. Fornisce un intervallo di scadenza predefinito nel caso in cui un particolare record di catalogo non contenga un valore di scadenza del catalogo o della vignetta valido, oppure se l'accesso diretto a un file di vignetta o a un file di materiale non avviene tramite un record di catalogo.
solution: Experience Manager
title: Scadenza
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Scadenza{#expiration}

Tempo predefinito della cache del client per la durata. Fornisce un intervallo di scadenza predefinito nel caso in cui un particolare record di catalogo non contenga un valore di catalogo valido::Scadenza o vignetta::Scadenza, o se si accede direttamente a un file di vignetta o a un file di materiale anziché tramite un record di catalogo.

## Proprietà {#section-8e2bade105ec4905ae5c4911f500279f}

Numero reale, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dei dati di risposta. Imposta su 0 per far scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Imposta su -1 per contrassegnare come *non scade*.

## Predefinito {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Ereditato da predefinito::Scadenza se non definito o se vuoto.

## Consultate anche {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalogo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [vignetta::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
