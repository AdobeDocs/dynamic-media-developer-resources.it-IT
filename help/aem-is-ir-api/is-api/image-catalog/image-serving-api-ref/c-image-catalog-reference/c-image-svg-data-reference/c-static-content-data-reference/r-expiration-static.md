---
description: Scadenza
solution: Experience Manager
title: Scadenza
topic: Scene7 Image Serving - Image Rendering API
uuid: a727bbfc-940b-4d65-96d6-b2159b70bac1
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---


# Scadenza{#expiration}

Utilizzato per gestire il caching dei client e dei server proxy. Il server calcola l’ora/data di scadenza dei dati di risposta HTTP aggiungendo questo valore all’ora/data di trasmissione.

I browser gestiscono le cache utilizzando i tempi di scadenza dei file. Prima di trasmettere una richiesta al server, il browser controlla la cache per verificare se il file è già stato scaricato. In questo caso, e se il file non è ancora scaduto, il browser invia una richiesta di GET condizionale (ad esempio con il campo If-Modified-Since impostato nell&#39;intestazione della richiesta) anziché una normale richiesta di GET. Il server ha la possibilità di rispondere con lo stato &#39;304&#39; e non trasmettere l&#39;immagine. Il browser carica quindi il file dalla cache. Ciò potrebbe aumentare notevolmente le prestazioni complessive per i dati a cui si accede di frequente.

La scadenza è utilizzata per i seguenti tipi di risposta:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Alcuni tipi di risposte (ad esempio, risposte di errore) sono sempre contrassegnate per la scadenza immediata (o con tag come non memorizzabili nella cache), mentre altri (ad esempio, risposte di proprietà o immagini predefinite) utilizzano impostazioni di scadenza speciali ( `attribute::NonImgExpiration` e `attribute::DefaultExpiration`).

## Proprietà {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Numero reale, -2, -1 o 0 o superiore. Numero di ore fino alla scadenza dalla generazione dell’immagine di risposta. Impostate su 0 per scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Impostare su -1 per contrassegnare come *`never expire`*. In questo caso, il server restituisce sempre lo stato 304 (non modificato) in risposta a richieste di GET condizionali senza verificare se il file è effettivamente cambiato. Impostare su -2 per utilizzare il valore predefinito fornito da `attribute::Expiration`.

## Predefinito {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` viene utilizzato se il campo non è presente, se il valore è -2 o se il campo è vuoto.

## Consultate anche {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
