---
description: Scadenza
solution: Experience Manager
title: Scadenza
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# Scadenza{#expiration}

Utilizzato per gestire la memorizzazione in cache del server client e proxy. Il server calcola l’ora/data di scadenza dei dati di risposta HTTP aggiungendo questo valore all’ora/data di trasmissione.

I browser gestiscono le cache utilizzando i tempi di scadenza dei file. Prima di passare una richiesta al server, il browser controlla la sua cache per vedere se il file è già stato scaricato. In tal caso, e se il file non è ancora scaduto, il browser invia una richiesta di GET condizionale (ad esempio con il campo If-Modified-Since impostato nell&#39;intestazione della richiesta) anziché una normale richiesta di GET. Il server ha la possibilità di rispondere con lo stato &#39;304&#39; e non trasmettere l&#39;immagine. Il browser carica quindi il file dalla sua cache. Ciò può aumentare notevolmente le prestazioni complessive per i dati a cui si accede di frequente.

La scadenza viene utilizzata per i seguenti tipi di risposta:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Alcuni tipi di risposte (ad esempio le risposte agli errori) sono sempre contrassegnate per la scadenza immediata (o con tag non memorizzabili nella cache), mentre altri (ad esempio, risposte alle proprietà o alle immagini predefinite) utilizzano impostazioni di scadenza speciali ( `attribute::NonImgExpiration` e `attribute::DefaultExpiration`).

## Proprietà {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Numero reale, -2, -1 o 0 o superiore. Numero di ore fino alla scadenza dalla generazione dell&#39;immagine di risposta. Imposta su 0 per far scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Imposta su -1 per contrassegnare come *`never expire`*. In questo caso il server restituisce sempre lo stato 304 (non modificato) in risposta a richieste di GET condizionali senza verificare se il file è effettivamente cambiato. Imposta su -2 per utilizzare il valore predefinito fornito da `attribute::Expiration`.

## Predefinito {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` viene utilizzato se il campo non è presente, se il valore è -2 o se il campo è vuoto.

## Consultate anche {#section-0e5e8595aad641c689726828712a8902}

[attributo::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [attributo::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attributo::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
