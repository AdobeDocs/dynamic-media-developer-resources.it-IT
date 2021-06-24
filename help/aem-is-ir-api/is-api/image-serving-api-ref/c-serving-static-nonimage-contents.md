---
description: È possibile utilizzare Image Server per gestire il contenuto non immagini nei cataloghi e distribuirlo tramite un contesto /is/content separato.
solution: Experience Manager
title: Distribuzione di contenuti statici (non immagine)
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Distribuzione di contenuti statici (non immagine){#serving-static-non-image-contents}

È possibile utilizzare Image Server per gestire il contenuto non immagini nei cataloghi e distribuirlo tramite un contesto /is/content separato.

Questa funzionalità consente di configurare il TTL per ogni elemento separatamente.

Image Serving supporta i seguenti comandi in [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type  </a> </p> </td> 
  <td class="stentry"> <p>Filtro del tipo di contenuto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req  </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>e  <span class="codeph"> req=exists  </span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache  </a> </p> </td> 
  <td class="stentry"> <p>Consente di disabilitare la memorizzazione in cache lato client. </p> </td> 
 </tr> 
</table>

## Sintassi di base {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> richiesta  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http://  <span class="varname"> server  </span>/is/content[/catalog/  <span class="varname"> item  </span>][? <span class="varname"> modificatori  </span>]  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ :  <span class="varname"> porta  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificatore del catalogo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID elemento di contenuto statico. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificatori  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> comando  </span>*[&amp;  <span class="varname"> comando  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> value  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>Uno dei nomi di comando supportati. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore comando. </p> </td> 
 </tr> 
</table>

## Cataloghi di contenuti statici {#section-91014f17f0d543d7aaf24539b2d7d4b9}

I cataloghi di contenuti statici sono simili ai cataloghi di immagini, ma supportano meno campi di dati:

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attributo/Dati </p> </th> 
   <th colname="col2" class="entry"> <p>Note </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::Id  </span> </p> </td> 
   <td colname="col2"> <p>Identificatore del record del catalogo per l'elemento di contenuto statico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::Percorso  </span> </p> </td> 
   <td colname="col2"> <p>Percorso file dell'elemento di contenuto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::Scadenza  </span> </p> </td> 
   <td colname="col2"> <p>TTL per questo elemento di contenuto; <span class="codeph"> attribute::Expiration </span> viene utilizzato se non specificato o se vuoto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Timestamp della modifica del file; obbligatorio quando la convalida basata su catalogo è abilitata con l'attributo <span class="codeph">::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::UserData  </span> </p> </td> 
   <td colname="col2"> <p>Metadati facoltativi associati a questo elemento di contenuto statico; disponibile per il client con <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::UserType  </span> </p> </td> 
   <td colname="col2"> <p>tipo di dati facoltativo; può essere utilizzato per filtrare le richieste di contenuto statico con il comando <span class="codeph"> type= </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrare il contenuto statico {#section-4c41bf41ff994910840c1352683d1f37}

Questo meccanismo può aiutare a garantire che i clienti ricevano solo i contenuti appropriati alle loro esigenze. Presupponendo che il contenuto statico sia dotato dei valori `catalog::UserType` appropriati, il client può aggiungere il comando `type=` alla richiesta. Image Serving confronta il valore fornito con il comando `type=` con il valore di `catalog::UserType` e, in caso di mancata corrispondenza, restituisce un errore invece di contenuti potenzialmente inappropriati.

## File di sottotitoli video {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

È possibile incapsulare file di sottotitoli video (WebVTT), CSS o qualsiasi file di testo in formato JSONP. La risposta JSON è descritta di seguito.

* Per i file WebVTT, il tipo mime della risposta è text/javascript. JSON non viene restituito; viene invece restituito Javascript che chiama un metodo con JSON. Sia l&#39;ID che il gestore sono facoltativi.
* Per i file CSS, il tipo mime della risposta è text/javascript. Sia l&#39;ID che il gestore sono facoltativi.
* Per impostazione predefinita, la codifica UTF-8 viene applicata per garantire che venga decodificata correttamente. Il limite di dimensione predefinito è di 2 MB.

È inoltre possibile utilizzare le tracce per altri tipi di metadati temporizzati. I dati di origine per ogni elemento di tracciamento sono un file di testo costituito da un elenco di suggerimenti temporizzati. I codici possono includere dati in formati come JSON o CSV.

Per ulteriori informazioni sul formato JSONP, consulta [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) .

Per ulteriori informazioni sul formato JSON, consulta [www.json.org](http://www.json.org) .

## Consultate anche {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Riferimento catalogo  [immagini](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
