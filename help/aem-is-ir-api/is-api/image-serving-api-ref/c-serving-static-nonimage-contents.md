---
title: Distribuzione di contenuti statici (non di immagine)
description: È possibile utilizzare Image Server per gestire i contenuti non di immagine nei cataloghi e distribuirli in un contesto /is/content separato.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Distribuzione di contenuti statici (non di immagine){#serving-static-non-image-contents}

È possibile utilizzare Image Server per gestire i contenuti non di immagine nei cataloghi e distribuirli in un contesto /is/content separato.

Questa funzionalità consente di configurare il TTL per ogni elemento separatamente.

Image Server supporta i seguenti comandi in [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> tipo </a> </p> </td> 
  <td class="stentry"> <p>Filtro del tipo di contenuto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>, e <span class="codeph"> req=exists </span> solo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache </a> </p> </td> 
  <td class="stentry"> <p>Consente di disabilitare il caching lato client. </p> </td> 
 </tr> 
</table>

## Sintassi di base {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> richiesta </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> elemento </span>][? <span class="varname"> modificatori </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> porta </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogo </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificatore del catalogo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> elemento </span> </span> </p> </td> 
  <td class="stentry"> <p>ID elemento contenuto statico. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificatori </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> comando </span>*[&amp; <span class="varname"> comando </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> comando </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> valore </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>Uno dei nomi di comando supportati. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valore </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore del comando. </p> </td> 
 </tr> 
</table>

## Cataloghi di contenuti statici {#section-91014f17f0d543d7aaf24539b2d7d4b9}

I cataloghi di contenuti statici sono simili ai cataloghi di immagini, ma supportano un numero inferiore di campi di dati:

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attributo/Dati </p> </th> 
   <th colname="col2" class="entry"> <p>Note </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::Id </span> </p> </td> 
   <td colname="col2"> <p>Identificatore del record di catalogo per questo elemento di contenuto statico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td colname="col2"> <p>Percorso del file per l'elemento di contenuto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::scadenza </span> </p> </td> 
   <td colname="col2"> <p>Il TTL per questo elemento di contenuto; <span class="codeph"> attribute::Scadenza </span> viene utilizzato se non specificato o se vuoto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::Timestamp </span> </p> </td> 
   <td colname="col2"> <p>Timestamp di modifica del file; obbligatorio quando la convalida basata sul catalogo è abilitata con <span class="codeph"> attribute::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::DatiUtente </span> </p> </td> 
   <td colname="col2"> <p>Metadati facoltativi associati a questo elemento di contenuto statico, disponibili per il client con <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Tipo di dati facoltativo; può essere utilizzato per filtrare le richieste di contenuto statico con <span class="codeph"> type=, comando </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtraggio del contenuto statico {#section-4c41bf41ff994910840c1352683d1f37}

Questo meccanismo può aiutare a garantire che i clienti ricevano solo i contenuti appropriati alle loro esigenze. Supponendo che il contenuto statico sia contrassegnato con i tag appropriati `catalog::UserType` , il client può aggiungere i `type=` alla richiesta. Image Server confronta il valore fornito con `type=` al valore di `catalog::UserType` e, in caso di mancata corrispondenza, restituisce un errore invece di contenuti potenzialmente inappropriati.

## File di didascalia video {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

È possibile incapsulare file di sottotitoli video (WebVTT), CSS o qualsiasi file di testo in formato JSONP. La risposta JSON è descritta di seguito.

* Per i file WebVTT, il tipo mime della risposta è text/javascript. JSON non viene restituito; viene invece restituito JavaScript che chiama un metodo con JSON. Sia l’ID che il gestore sono facoltativi.
* Per i file CSS, il tipo mime della risposta è text/javascript. Sia l’ID che il gestore sono facoltativi.
* Per impostazione predefinita, viene applicata la codifica UTF-8 per garantire che venga decodificata correttamente. Il limite predefinito è 2 MB.

È inoltre possibile utilizzare tracce per altri tipi di metadati temporizzati. I dati di origine di ciascun elemento del brano sono un file di testo composto da un elenco di segnali temporizzati. Le cue possono includere dati in formati come JSON o CSV.

Consulta [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) per ulteriori informazioni sul formato JSONP.

Consulta [www.json.org](https://www.json.org/json-en.html) per ulteriori informazioni sul formato JSON.

## Consultate anche {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Riferimento catalogo immagini](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
