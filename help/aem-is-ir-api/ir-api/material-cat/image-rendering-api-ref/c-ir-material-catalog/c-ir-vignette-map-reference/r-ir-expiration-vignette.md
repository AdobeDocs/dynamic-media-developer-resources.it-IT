---
description: Durata cache client. Numero di ore fino alla scadenza. Utilizzato per gestire il caching dei client e dei server proxy.
seo-description: Durata cache client. Numero di ore fino alla scadenza. Utilizzato per gestire il caching dei client e dei server proxy.
seo-title: Scadenza
solution: Experience Manager
title: Scadenza
topic: Scene7 Image Serving - Image Rendering API
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Scadenza{#expiration}

Durata cache client. Numero di ore fino alla scadenza. Utilizzato per gestire il caching dei client e dei server proxy.

Vedere ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` per informazioni dettagliate.

## Proprietà {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Numero reale, -2, -1, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dell’immagine di risposta. Impostate su 0 per scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Impostare su -1 per contrassegnare come `never expire`; in questo caso, il server restituisce sempre lo stato 403 in risposta alle richieste condizionali `GET` senza verificare se il file è effettivamente cambiato. Impostare su -2 per utilizzare il valore predefinito fornito da `attribute::Expiration`.

## Predefinito {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` viene utilizzato se il campo non è presente, se il valore è -2 o se il campo è vuoto.

## Consultate anche {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attributo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalogo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
