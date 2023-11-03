---
description: Distribuzione di contenuto statico (non di immagine)
solution: Experience Manager
title: Distribuzione di contenuto statico (non di immagine)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---

# Distribuzione di contenuto statico (non di immagine){#serving-static-non-image-content}

Image Server offre un meccanismo per gestire contenuti non di immagine in cataloghi e distribuirli tramite un’applicazione separata `context /is/content`. Il meccanismo consente di configurare il TTL per ogni elemento separatamente.

## Sintassi di base {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> richiesta </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> server </span>/is/content[/ <span class="varname"> catalogo </span>/ <span class="varname"> elemento </span>][? <span class="varname"> modificatori </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> porta </span>] </span> </p> </td> 
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

## Panoramica dei comandi {#section-61657a0141914053ab12038ad7e91500}

Image Server supporta i seguenti comandi in /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> tipo </a> </td> 
  <td class="stentry"> <p>Filtro del tipo di contenuto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>, e <span class="codeph"> req=exists </span> solo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache </a> </td> 
  <td class="stentry"> <p>Consente di disabilitare il caching lato client. </p> </td> 
 </tr> 
</table>

## Cataloghi di contenuti statici {#section-b2b8f4860fe84e528493ed704c7c5141}

I cataloghi di contenuti statici sono simili ai cataloghi di immagini, ma supportano un numero inferiore di campi di dati:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attributo/Dati</b> </th> 
   <th class="entry"> <b> Note</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Id </span> </p> </td> 
   <td> <p> Identificatore del record di catalogo per questo elemento di contenuto statico </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td> <p> Percorso file per l'elemento di contenuto </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::scadenza </span> </p> </td> 
   <td> <p> Il TTL per questo contenuto; attributo::Expiration viene utilizzato se non specificato o se vuoto </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Timestamp </span> </p> </td> 
   <td> <p> Timestamp di modifica del file; obbligatorio quando la convalida basata sul catalogo è abilitata con l'attributo::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::DatiUtente </span> </p> </td> 
   <td> <p> Metadati facoltativi associati a questo elemento di contenuto statico, disponibili per il client con req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td> <p> Tipo di dati facoltativo; può essere utilizzato per filtrare le richieste di contenuto statico con il comando type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtraggio del contenuto statico {#section-896c37cf68bc446eb0766fb378898262}

Questo meccanismo può aiutare a garantire che i clienti ricevano solo i contenuti appropriati alle loro esigenze. Supponendo che il contenuto statico sia contrassegnato con i tag appropriati `catalog::UserType`, il client può aggiungere i `type=` alla richiesta. Image Server confronta il valore fornito con `type=` al valore di `catalog::UserType` e, in caso di mancata corrispondenza, restituisce un errore invece di contenuti potenzialmente inappropriati.

## Consultate anche {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Riferimento catalogo immagini](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
