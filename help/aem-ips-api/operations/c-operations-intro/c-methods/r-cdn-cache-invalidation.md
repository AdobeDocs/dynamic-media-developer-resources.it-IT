---
description: Inoltra l’elenco di URL fornito al provider Dynamic Media CDN (Content Distribution Network) per invalidare la cache esistente delle risposte HTTP.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 3%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Inoltra l’elenco di URL fornito al provider Dynamic Media CDN (Content Distribution Network) per invalidare la cache esistente delle risposte HTTP.

## cdnCacheInvalidation: Informazioni su {#section-4f70d2bc79d64288b961836ab17e9690}

L’annullamento della validità della cache CDN forza la riconvalida di tutte le richieste HTTP per questi URL rispetto ai dati pubblicati correnti sulla rete Dynamic Media dopo che questa richiesta di invalidazione è stata elaborata tramite la rete CDN. Eventuali URL non collegati alla struttura URL del servizio Dynamic Media e che corrispondono direttamente all’ID radice della società Dynamic Media assegnato al momento della creazione della società genereranno un errore API per l’intera richiesta. Anche gli URL non validi che la CDN non supporta e che considera non validi genereranno un errore API per l’intera richiesta.

**Frequenza di utilizzo: Regole**

Le regole che disciplinano la frequenza di utilizzo di questa funzione sono controllate dai partner CDN di Dynamic Media. La CDN mantiene la discrezionalità di degradare la reattività di questi invalidamenti per mantenere prestazioni ottimali del suo servizio per i suoi utenti. Se Dynamic Media dovesse ricevere una notifica relativa all’utilizzo eccessivo di questa funzione, dovremo ricorrere alla disattivazione della funzione a livello aziendale o interamente nell’intero servizio.

**E-mail di conferma**

Le e-mail di conferma dal partner CDN di Dynamic Media possono essere inviate al creatore dell’elenco o fino a 5 altri indirizzi e-mail. L’API invia la conferma quando l’intera rete CDN viene informata che gli URL a cui si fa riferimento nell’e-mail sono stati cancellati. Una singola chiamata a `cdnCacheInvalidation` può inviare più e-mail se il numero di URL forniti supera il numero che Dynamic Media può consegnare al partner CDN in una singola notifica. Attualmente, questo si verifica se la richiesta supera i 100 URL, ma è soggetta a modifiche in base alla richiesta del partner CDN.

**Supportato da**

6,0

## Tipi di utenti autorizzati {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parametri {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** (  `cdnCacheInvalidationParam`)

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
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Sì </p> </td> 
   <td> <p> L’handle dell’azienda connessa agli URL da annullare la validità. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> tipi:UrlArray</span> </p> </td> 
   <td> <p> Sì </p> </td> 
   <td> <p> Elenco di fino a 1000 URL da annullare la validità dalla cache CDN. Tutti gli URL devono contenere l’ID radice della società Dynamic Media per essere invalidati. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**(  `cdnCacheInvalidationReturn`)

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
   <td colname="col4"> <p>Un handle che fa riferimento alla richiesta di eliminazione. </p> <p>L'API <span class="codeph"> cdnCacheInvalidation</span> ora invalida la cache quasi immediatamente (~5 secondi). Di conseguenza, non è più necessario eseguire il polling per lo stato di invalidazione. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> EstimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>secondi stimati al completamento della richiesta di eliminazione. I clienti devono attendere questo momento prima di procedere al polling. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-f414361a58e84dfcbbac30a358d02125}

Questo esempio richiede l’annullamento della validità di quattro URL nella cache CDN. La risposta contiene il conteggio sintetico del successo delle operazioni e un elenco di dettagli di errore forniti direttamente dalla CDN per aiutare il cliente nell&#39;utilizzo di questa funzione.

`getCdnCacheInvalidationStatus` funzionamento.

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

