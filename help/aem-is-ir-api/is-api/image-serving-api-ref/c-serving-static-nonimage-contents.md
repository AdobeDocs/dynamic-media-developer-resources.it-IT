---
description: È possibile utilizzare Image Server per gestire i contenuti non immagine nei cataloghi e distribuirli in un contesto diverso da /is/content.
seo-description: È possibile utilizzare Image Server per gestire i contenuti non immagine nei cataloghi e distribuirli in un contesto diverso da /is/content.
seo-title: Trasmissione di contenuti statici (non immagini)
solution: Experience Manager
title: Trasmissione di contenuti statici (non immagini)
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---


# Trasmissione di contenuti statici (non immagini){#serving-static-non-image-contents}

È possibile utilizzare Image Server per gestire i contenuti non immagine nei cataloghi e distribuirli in un contesto diverso da /is/content.

Questa funzionalità consente di configurare il TTL per ogni elemento separatamente.

Image Server supporta i seguenti comandi in [!DNL /is/content]:

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
  <td class="stentry"> <p>Consente di disattivare il caching lato client. </p> </td> 
 </tr> 
</table>

## Sintassi di base {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> request  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http://  <span class="varname"> server  </span>/is/content[/catalog/  <span class="varname"> item  </span>][? <span class="varname"> modificatori  </span>]  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ :  <span class="varname"> porta  </span>]  </span> </p> </td> 
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

## Cataloghi di contenuti statici {#section-91014f17f0d543d7aaf24539b2d7d4b9}

I cataloghi di contenuti statici sono simili ai cataloghi di immagini, ma supportano un numero minore di campi dati:

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
   <td colname="col2"> <p>Identificatore del record del catalogo per questo elemento di contenuto statico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo:Percorso  </span> </p> </td> 
   <td colname="col2"> <p>Percorso del file per l'elemento di contenuto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::Scadenza  </span> </p> </td> 
   <td colname="col2"> <p>TTL per questo elemento di contenuto; <span class="codeph"> attribute::Expiration </span> è utilizzato se non è specificato o se è vuoto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::TimeStamp  </span> </p> </td> 
   <td colname="col2"> <p>Timestamp modifica file; obbligatorio quando la convalida basata su catalogo è abilitata con l'attributo <span class="codeph">::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::UserData  </span> </p> </td> 
   <td colname="col2"> <p>Metadati facoltativi associati a questo elemento di contenuto statico; disponibile per il client con <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogo::UserType  </span> </p> </td> 
   <td colname="col2"> <p>Tipo di dati opzionale; può essere utilizzato per filtrare le richieste di contenuto statico con il comando <span class="codeph"> type= </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtro del contenuto statico {#section-4c41bf41ff994910840c1352683d1f37}

Questo meccanismo consente di garantire che i clienti ricevano solo contenuti adatti alle loro esigenze. Presupponendo che al contenuto statico siano assegnati tag con valori `catalog::UserType` appropriati, il client può aggiungere il comando `type=` alla richiesta. Image Serving confronta il valore fornito con il comando `type=` con il valore di `catalog::UserType` e, in caso di mancata corrispondenza, restituisce un errore invece di contenuti potenzialmente inappropriati.

## File di sottotitoli video {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Potete incorporare file di sottotitoli video (WebVTT), CSS o qualsiasi file di testo in formato JSONP. La risposta JSON è descritta di seguito.

* Per i file WebVTT, il tipo mime della risposta è text/javascript. JSON non viene restituito; viene invece restituito Javascript che chiama un metodo con JSON. ID e gestore sono entrambi facoltativi.
* Per i file CSS, il tipo mime della risposta è text/javascript. ID e gestore sono entrambi facoltativi.
* Per impostazione predefinita, la codifica UTF-8 viene applicata per garantire che venga decodificata correttamente. Il limite di dimensione predefinito è 2 MB.

Potete anche usare le tracce per altri tipi di metadati temporizzati. I dati di origine per ciascun elemento di tracciamento sono un file di testo composto da un elenco di segnali temporizzati. Cue può includere dati in formati come JSON o CSV.

Per ulteriori informazioni sul formato JSONP, vedere [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP).

Per ulteriori informazioni sul formato JSON, consultate [www.json.org](http://www.json.org).

## Consultate anche {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Riferimento catalogo  [immagini](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
