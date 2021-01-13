---
description: Trasmissione di contenuti statici (non immagini)
solution: Experience Manager
title: Trasmissione di contenuti statici (non immagini)
topic: Scene7 Image Serving - Image Rendering API
uuid: 4ec483fe-68a4-4ae2-b5ce-730229a9bc15
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Trasmissione di contenuto statico (non immagine){#serving-static-non-image-content}

Image Serving fornisce un meccanismo per gestire i contenuti non immagine nei cataloghi e distribuirli tramite un `context /is/content` separato. Il meccanismo consente di configurare il TTL per ogni elemento separatamente.

## Sintassi di base {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> request  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http://  <span class="varname"> server  </span>/is/content[/  <span class="varname"> catalogo  </span>/  <span class="varname"> elemento  </span>][? <span class="varname"> modificatori  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[:  <span class="varname"> porta  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogo  </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificatore catalogo. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID elemento contenuto statico. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificatori  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span>*[&amp;  <span class="varname"> command  </span>]  </span> </p> </td> 
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

## Panoramica dei comandi {#section-61657a0141914053ab12038ad7e91500}

Image Server supporta i seguenti comandi in /is/content:

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type  </a> </td> 
  <td class="stentry"> <p>Filtro del tipo di contenuto. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req  </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>e  <span class="codeph"> req=exists  </span> only. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache  </a> </td> 
  <td class="stentry"> <p>Consente di disattivare il caching lato client. </p> </td> 
 </tr> 
</table>

## Cataloghi di contenuti statici {#section-b2b8f4860fe84e528493ed704c7c5141}

I cataloghi di contenuti statici sono simili ai cataloghi di immagini, ma supportano un numero minore di campi dati:

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attributo/Dati</b> </th> 
   <th class="entry"> <b> Note</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Id  </span> </p> </td> 
   <td> <p> Identificatore del record del catalogo per questo elemento di contenuto statico </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo:Percorso  </span> </p> </td> 
   <td> <p> Percorso del file per l'elemento di contenuto </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Scadenza  </span> </p> </td> 
   <td> <p> TTL per questo elemento di contenuto; attribute::La scadenza è utilizzata se non è specificata o se è vuota </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::TimeStamp  </span> </p> </td> 
   <td> <p> Timestamp modifica file; obbligatorio quando la convalida basata su catalogo è abilitata con l'attributo::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::UserData  </span> </p> </td> 
   <td> <p> Metadati facoltativi associati a questo elemento di contenuto statico; disponibile per il client con req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::UserType  </span> </p> </td> 
   <td> <p> Tipo di dati opzionale; può essere utilizzato per filtrare le richieste di contenuto statico con il comando type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtro del contenuto statico {#section-896c37cf68bc446eb0766fb378898262}

Questo meccanismo consente di garantire che i clienti ricevano solo contenuti adatti alle loro esigenze. Presupponendo che al contenuto statico siano assegnati tag con valori `catalog::UserType`appropriati, il client può aggiungere il comando `type=` alla richiesta. Image Serving confronterà il valore fornito con il comando `type=` con il valore di `catalog::UserType` e, in caso di mancata corrispondenza, restituirà un errore invece di contenuti potenzialmente inappropriati.

## Consultate anche {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Riferimento catalogo  [immagini](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
