---
description: Tempo di esecuzione della cache del client. Numero di ore fino alla scadenza. Utilizzato per gestire la memorizzazione in cache del server client e proxy.
solution: Experience Manager
title: Scadenza
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# Scadenza{#expiration}

Tempo di esecuzione della cache del client. Numero di ore fino alla scadenza. Utilizzato per gestire la memorizzazione in cache del server client e proxy.

Per ulteriori informazioni, vedere ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` .

## Proprietà {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Numero reale, -2, -1, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dell&#39;immagine di risposta. Imposta su 0 per far scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Impostare su -1 per contrassegnare come `never expire`; in questo caso il server restituisce sempre lo stato 403 in risposta alle richieste condizionali `GET` senza verificare se il file è effettivamente cambiato. Imposta su -2 per utilizzare il valore predefinito fornito da `attribute::Expiration`.

## Predefinito {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` viene utilizzato se il campo non è presente, se il valore è -2 o se il campo è vuoto.

## Consultate anche {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attributo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalogo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
