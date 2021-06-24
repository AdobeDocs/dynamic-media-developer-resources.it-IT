---
description: Versione immagine/metadati. Quando si lavora con contenuti che cambiano frequentemente, i server in reti di caching come Akamai, cache del browser e cache del server proxy aziendale possono memorizzare le risposte Image Server che potrebbero non essere aggiornate per periodi di tempo.
solution: Experience Manager
title: Id
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 2%

---

# Id{#id}

Versione immagine/metadati. Quando si lavora con contenuti che cambiano frequentemente, i server in reti di caching come Akamai, cache del browser e cache del server proxy aziendale possono memorizzare le risposte Image Server che potrebbero non essere aggiornate per periodi di tempo.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>Stringa di versione. </p> </td> 
 </tr> 
</table>

Image Serving include un meccanismo di controllo delle versioni che può aiutare a ridurre la possibilità che un&#39;applicazione utilizzi una voce cache obsoleta. Questo meccanismo prevede l&#39;utilizzo di `req=props` per ottenere le stringhe dell&#39;identificatore di versione per i dati immagine e i metadati (come la mappa immagine o i dati di destinazione dello zoom). La stringa dell&#39;identificatore di versione viene quindi aggiunta alle richieste Image Serving memorizzabili nella cache con il comando `id=` .

Quando un&#39;immagine sorgente o i metadati cambiano, cambia anche il valore dell&#39;ID versione corrispondente. L’inclusione di un valore ID versione aggiornato con il comando `id=` garantisce che non sarà più possibile accedere alle vecchie voci di cache.

Nella tabella seguente sono elencate le stringhe relative all’identificatore di versione da utilizzare per ciascun tipo `req=`:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> identificatore di versione da req=props</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> map </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> maschera </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> target </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tam </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> dati utente </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` i tipi non elencati sopra dispongono di un TTL breve (  `attribute::NonImgExpiration`) o le loro risposte non sono affatto memorizzabili in cache; non vi è alcun vantaggio nell&#39;includere  `id=` tali richieste.

## Proprietà {#section-62e973d0d5884abebbb0679f9278ae2c}

Attributo di richiesta. Facoltativo. Sempre ignorato dal server.

## Predefinito {#section-96136720c82842c89505347ec39e6024}

Nessuno.

## Esempio {#section-a5fb871e0ec8485c91c4fca78895d17f}

Per esempio, vedere la descrizione di [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) .

## Vedi anche {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
