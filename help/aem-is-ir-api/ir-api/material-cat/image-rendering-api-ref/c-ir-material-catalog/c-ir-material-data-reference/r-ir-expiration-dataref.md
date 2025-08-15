---
title: Scade
description: Durata cache client. Numero di ore fino alla scadenza. Utilizzato per gestire il caching del client e del server proxy.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---

# Scade{#expiration}

Durata cache client. Numero di ore fino alla scadenza. Utilizzato per gestire il caching del client e del server proxy.

Il server calcola l&#39;ora/data di scadenza dei dati di risposta NTTP aggiungendo questo valore all&#39;ora/data di trasmissione.

I browser gestiscono le cache utilizzando i tempi di scadenza dei file. Prima di trasmettere una richiesta al server, il browser controlla la cache per verificare se il file è già stato scaricato. In tal caso, e se il file non è ancora scaduto, il browser invia una richiesta GET condizionale (ad esempio con l’intestazione della richiesta HTTP If-Modified-Since) anziché una normale richiesta GET. Il server ha la possibilità di rispondere con lo stato &quot;304&quot; e di non trasmettere l&#39;immagine. Il browser carica quindi semplicemente il file dalla propria cache. Questo può aumentare notevolmente le prestazioni complessive per i dati a cui si accede di frequente.

Il server imposta l&#39;intestazione di risposta HTTP Scadenza sulla data/ora corrente più il più piccolo dei valori di vignettatura::Scadenza e tutti i valori di catalogo::Scadenza per la vignettatura e tutti i materiali coinvolti nell&#39;operazione di rendering.

La scadenza è impostata principalmente per le risposte dei dati immagine. Alcuni tipi di risposte sono sempre contrassegnati per la scadenza immediata (o contrassegnati come non memorizzabili in cache), comprese tutte le risposte di errore o di proprietà.

## Proprietà {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Numero reale, -2, -1, 0 o superiore. Numero di ore mancanti alla scadenza dalla generazione dell’immagine di risposta. Impostate questo valore su 0 per far scadere immediatamente l&#39;immagine di risposta e disabilitare quindi la memorizzazione nella cache del client. Imposta su -1 per contrassegnare come `never expire`. In questo caso il server restituisce sempre lo stato 304 (non modificato) in risposta alle richieste condizionali `GET` senza verificare se il file è stato effettivamente modificato. Impostare su -2 per utilizzare il valore predefinito fornito da `attribute::Expiration`.

## Predefinito {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` viene utilizzato se il campo non è presente, se il valore è -2 o se il campo è vuoto.

## Consultate anche {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attributo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [vignettatura::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
