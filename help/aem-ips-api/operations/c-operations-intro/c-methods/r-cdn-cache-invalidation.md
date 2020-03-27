---
description: Invia l’elenco di URL fornito al provider CDN (Content Distribution Network) di Scene7 per annullare la validità della cache delle risposte HTTP.
seo-description: Invia l’elenco di URL fornito al provider CDN (Content Distribution Network) di Scene7 per annullare la validità della cache delle risposte HTTP.
seo-title: cdnCacheInvalidation
solution: Experience Manager
title: cdnCacheInvalidation
topic: Scene7 Image Production System API
uuid: 16cf53d4-4101-405c-b008-009b6ac62169
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Invia l’elenco di URL fornito al provider CDN (Content Distribution Network) di Scene7 per annullare la validità della cache delle risposte HTTP.

## cdnCacheInvalidation: Informazioni {#section-4f70d2bc79d64288b961836ab17e9690}

L’annullamento della validità della cache CDN forza la convalida di tutte le richieste HTTP per questi URL rispetto ai dati pubblicati correnti sulla rete Scene7, una volta elaborata la richiesta di annullamento della validità tramite la rete CDN. Eventuali URL che non sono collegati alla struttura URL del servizio Scene7 e che corrispondono direttamente all’ID radice della società di Scene7 assegnato al momento della creazione della società genereranno un errore API per l’intera richiesta. Eventuali URL non validi che la CDN non supporta e che considera non validi causeranno un errore API per l’intera richiesta.

**Frequenza di utilizzo: Regole**

Le regole che regolano la frequenza di utilizzo di questa funzione sono controllate dai partner CDN di Scene7. La CDN mantiene la discrezione di ridurre la reattività di queste invalide per mantenere prestazioni ottimali del suo servizio per gli utenti. Se Scene7 dovesse ricevere una notifica di utilizzo eccessivo di questa funzione, dovrete disattivare la funzione a livello di singola azienda o in tutto il servizio.

**E-mail di conferma**

I messaggi e-mail di conferma inviati dal partner CDN di Scene7 possono essere inviati al creatore dell’elenco o fino a 5 altri indirizzi e-mail. L’API invia la conferma quando l’intera rete CDN riceve una notifica dell’eliminazione degli URL a cui si fa riferimento nell’e-mail. Una singola chiamata per `cdnCacheInvalidation` inviare più e-mail se il numero di URL forniti supera il numero che Scene7 può inviare al partner CDN con una singola notifica. Al momento, ciò si verifica se la richiesta supera i 100 URL, ma è soggetta a modifiche su richiesta del partner CDN.

**Supportato da**

6.0

## Tipi di utenti autorizzati {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parametri {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Nome</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Obbligatorio</b> </th> 
   <th class="entry"> <b> Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span></span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Sì </p> </td> 
   <td> <p> L’handle della società collegata agli URL per annullare la validità. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span></span> </p> </td> 
   <td> <p> <span class="codeph"> tipi:UrlArray</span> </p> </td> 
   <td> <p> Sì </p> </td> 
   <td> <p> Elenco di fino a 1000 URL da annullare la validità dalla cache CDN. Tutti gli URL devono contenere l’ID radice della società di Scene7 per essere invalidati. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Nome</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Obbligatorio</b> </th> 
   <th class="entry"> <b> Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Un handle che fa riferimento alla richiesta di eliminazione. </p> <p>L'API <span class="codeph"> cdnCacheInvalidation</span> ora invalida la cache quasi immediatamente (circa 5 secondi). Di conseguenza, il polling per lo stato di annullamento della validità in genere non è più necessario. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> EstimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>secondi stimati al completamento della richiesta di eliminazione. I client devono attendere questo momento prima di eseguire il sondaggio. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-f414361a58e84dfcbbac30a358d02125}

In questo esempio vengono richiesti quattro URL da annullare nella cache CDN. La risposta contiene un riepilogo dei conteggi del successo delle operazioni e un elenco dei dettagli di errore forniti direttamente dalla rete CDN per assistere il cliente nell&#39;utilizzo di questa funzione.

`getCdnCacheInvalidationStatus` operation.

**Request Contents (Richiesta contenuto)**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**Risposta**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

