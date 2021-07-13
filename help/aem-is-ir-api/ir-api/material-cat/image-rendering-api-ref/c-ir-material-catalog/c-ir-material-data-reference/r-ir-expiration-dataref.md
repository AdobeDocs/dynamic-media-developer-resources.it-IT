---
description: Tempo di esecuzione della cache del client. Numero di ore fino alla scadenza. Utilizzato per gestire la memorizzazione in cache del server client e proxy.
solution: Experience Manager
title: Scadenza
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# Scadenza{#expiration}

Tempo di esecuzione della cache del client. Numero di ore fino alla scadenza. Utilizzato per gestire la memorizzazione in cache del server client e proxy.

Il server calcola l’ora/data di scadenza dei dati di risposta NTTP aggiungendo tale valore all’ora/data di trasmissione.

I browser gestiscono le cache utilizzando i tempi di scadenza dei file. Prima di passare una richiesta al server, il browser controllerà la sua cache per vedere se il file è già stato scaricato. In tal caso e se il file non è ancora scaduto, il browser invia una richiesta di GET condizionale (ad esempio con l’intestazione di richiesta HTTP If-Modified-Since ) anziché una normale richiesta di GET. Il server ha la possibilità di rispondere con lo stato &#39;304&#39; e non trasmettere l&#39;immagine. Il browser carica quindi semplicemente il file dalla sua cache. Ciò può aumentare notevolmente le prestazioni complessive per i dati a cui si accede di frequente.

Il server imposterà l&#39;intestazione di risposta HTTP della scadenza alla data/ora corrente più la più piccola di vignetta::Scadenza e tutti i valori di catalogo::Scadenza per la vignetta e tutti i materiali coinvolti nell&#39;operazione di rendering.

La scadenza è impostata principalmente per le risposte ai dati immagine. Alcuni tipi di risposte saranno sempre contrassegnati per la scadenza immediata (o con tag come non memorizzabili nella cache), comprese tutte le risposte agli errori o alle risposte alle proprietà.

## Proprietà {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Numero reale, -2, -1, 0 o superiore. Numero di ore fino alla scadenza dalla generazione dell&#39;immagine di risposta. Imposta su 0 per far scadere sempre l&#39;immagine di risposta immediatamente, il che disabilita in modo efficace il caching del client. Imposta su -1 per contrassegnare come `never expire`. In questo caso il server restituisce sempre lo stato 304 (non modificato) in risposta a richieste `GET` condizionali senza verificare se il file è effettivamente modificato. Imposta su -2 per utilizzare il valore predefinito fornito da `attribute::Expiration`.

## Predefinito {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` viene utilizzato se il campo non è presente, se il valore è -2 o se il campo è vuoto.

## Consultate anche {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attributo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [vignetta::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
