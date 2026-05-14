---
description: Durata cache client. Numero di ore fino alla scadenza. Utilizzato per gestire il caching del client e del server proxy.
solution: Experience Manager
title: Scade
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
TQID: 'https://experienceleague.adobe.com/VHARdBKoak-pB54FrPO6u0Gpmd-1sQZUF-78j3ixB2U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 2%

---

# Scade{#expiration}

Durata cache client. Numero di ore fino alla scadenza. Utilizzato per gestire il caching del client e del server proxy.

Per ulteriori dettagli, vedere [catalogo::Scadenza](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md).

## Proprietà {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Numero reale, -2, -1, 0 o superiore. Numero di ore mancanti alla scadenza dalla generazione dell’immagine di risposta. Impostate questo valore su 0 per far scadere immediatamente l&#39;immagine di risposta e disabilitare quindi la memorizzazione nella cache del client. Impostare su -1 per contrassegnare come `never expire`; in questo caso il server restituisce sempre lo stato 403 in risposta alle richieste condizionali `GET` senza verificare se il file è stato effettivamente modificato. Impostare su -2 per utilizzare il valore predefinito fornito da `attribute::Expiration`.

## Predefinito {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` viene utilizzato se il campo non è presente, se il valore è -2 o se il campo è vuoto.

## Consultate anche {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attributo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [catalogo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
