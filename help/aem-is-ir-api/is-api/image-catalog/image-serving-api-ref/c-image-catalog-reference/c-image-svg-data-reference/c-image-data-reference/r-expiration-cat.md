---
title: Scade
description: Utilizzato per gestire il caching del client e del server proxy. Il server calcola l’ora/data di scadenza dei dati di risposta HTTP aggiungendo questo valore all’ora/data di trasmissione.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee329834-a2a0-44fd-a0a5-7bf5a8e0a5a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---

# Scade{#expiration}

Utilizzato per gestire il caching del client e del server proxy. Il server calcola l’ora/data di scadenza dei dati di risposta HTTP aggiungendo questo valore all’ora/data di trasmissione.

I browser gestiscono le cache utilizzando i tempi di scadenza dei file. Prima di trasmettere una richiesta al server, il browser controlla la cache per verificare se il file è già stato scaricato. In tal caso, e se il file non è ancora scaduto, il browser invia una richiesta di GET condizionale (ad esempio con il campo If-Modified-Since impostato nell&#39;intestazione della richiesta) anziché una normale richiesta di GET. Il server ha la possibilità di rispondere con lo stato &quot;304&quot; e di non trasmettere l&#39;immagine. Il browser carica quindi il file dalla propria cache. Questo può aumentare notevolmente le prestazioni complessive per i dati a cui si accede di frequente.

La scadenza viene utilizzata per i seguenti tipi di risposta:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Alcuni tipi di risposte (ad esempio, le risposte di errore) sono sempre contrassegnati per la scadenza immediata (o contrassegnati come non memorizzabili in cache), mentre altri (ad esempio, le risposte di proprietà o immagini predefinite) utilizzano impostazioni di scadenza speciali ( `attribute::NonImgExpiration` e `attribute::DefaultExpiration`).

## Proprietà {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Numero reale, -2, -1 o 0 o superiore. Numero di ore mancanti alla scadenza dalla generazione dell’immagine di risposta. Impostate questo valore su 0 per far scadere immediatamente l&#39;immagine di risposta, disattivando di fatto la memorizzazione in cache del client. Imposta su -1 per contrassegnare come *`never expire`*. In questo caso, il server restituisce sempre lo stato 304 (non modificato) in risposta alle richieste di GET condizionale senza verificare se il file è stato effettivamente modificato. Imposta su -2 per utilizzare il valore predefinito fornito da `attribute::Expiration`.

## Predefinito {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` viene utilizzato se il campo non è presente, se il valore è -2 o se il campo è vuoto.

## Consultate anche {#section-0e5e8595aad641c689726828712a8902}

[attribute::Scadenza](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
