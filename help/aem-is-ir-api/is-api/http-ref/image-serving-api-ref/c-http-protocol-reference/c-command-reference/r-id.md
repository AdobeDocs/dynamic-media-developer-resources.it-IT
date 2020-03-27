---
description: Versione immagine/metadati Quando si lavora con contenuti che si modificano frequentemente, i server nelle reti di caching come Akamai, nelle cache del browser e nelle cache dei server proxy aziendali possono memorizzare le risposte Image Server che potrebbero essere non aggiornate per periodi di tempo.
seo-description: Versione immagine/metadati Quando si lavora con contenuti che si modificano frequentemente, i server nelle reti di caching come Akamai, nelle cache del browser e nelle cache dei server proxy aziendali possono memorizzare le risposte Image Server che potrebbero essere non aggiornate per periodi di tempo.
seo-title: Id
solution: Experience Manager
title: Id
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Id{#id}

Versione immagine/metadati Quando si lavora con contenuti che si modificano frequentemente, i server nelle reti di caching come Akamai, nelle cache del browser e nelle cache dei server proxy aziendali possono memorizzare le risposte Image Server che potrebbero essere non aggiornate per periodi di tempo.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span></span> </p> </td> 
  <td class="stentry"> <p>Stringa della versione. </p> </td> 
 </tr> 
</table>

Image Serving include un meccanismo di controllo delle versioni che consente di ridurre la possibilità che un’applicazione utilizzi una voce cache obsoleta. Questo meccanismo prevede l’utilizzo `req=props` per ottenere le stringhe dell’identificatore di versione per i dati immagine e i metadati (ad esempio, mappe immagine o dati di destinazione di zoom). La stringa dell’identificatore di versione viene quindi aggiunta alle richieste Image Server memorizzabili nella cache con il `id=` comando .

Quando un&#39;immagine sorgente o i metadati cambiano, cambia anche il valore ID versione corrispondente. L&#39;inclusione di un ID versione aggiornato con il `id=` comando assicura che non sarà più possibile accedere alle vecchie voci della cache.

Nella tabella seguente sono elencate le stringhe dell&#39;identificatore di versione da utilizzare per ciascun `req=` tipo:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> identificatore versione da req=props</b> </th> 
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
   <td> <p> mask </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> target </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` i tipi non elencati sopra dispongono di un TTL breve ( `attribute::NonImgExpiration`) o le loro risposte non sono affatto memorizzabili nella cache; non vi è alcun vantaggio da includere `id=` con tali richieste.

## Proprietà {#section-62e973d0d5884abebbb0679f9278ae2c}

Attributo di richiesta. Facoltativo. Sempre ignorato dal server.

## Predefinito {#section-96136720c82842c89505347ec39e6024}

Nessuno.

## Esempio {#section-a5fb871e0ec8485c91c4fca78895d17f}

Consultate la descrizione di [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) , ad esempio l’utilizzo.

## See Also {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalogo::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
