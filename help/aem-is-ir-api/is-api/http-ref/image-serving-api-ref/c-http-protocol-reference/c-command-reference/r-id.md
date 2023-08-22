---
title: id
description: Versione immagine/metadati. Quando si lavora con contenuti che cambiano frequentemente, i server nelle reti di memorizzazione in cache come Akamai, nelle cache del browser e nelle cache dei server proxy aziendali possono memorizzare le risposte Image Server che potrebbero essere obsolete per periodi di tempo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# id{#id}

Versione immagine/metadati. Quando si lavora con contenuti che cambiano frequentemente, i server nelle reti di memorizzazione in cache come Akamai, nelle cache del browser e nelle cache dei server proxy aziendali possono memorizzare le risposte Image Server che potrebbero essere obsolete per periodi di tempo.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Stringa di versione. </p> </td> 
 </tr> 
</table>

Image Server include un meccanismo di controllo delle versioni che può aiutare a ridurre la possibilità che un’applicazione utilizzi una voce di cache obsoleta. Questo meccanismo comporta l’utilizzo di `req=props` per ottenere stringhe di identificatori di versione per i dati immagine e metadati (come i dati mappa immagine o destinazione di zoom). La stringa dell’identificatore della versione viene quindi aggiunta alle richieste memorizzabili in cache da Image Server con `id=` comando.

Quando un’immagine sorgente o i metadati cambiano, cambia anche il valore dell’ID versione corrispondente. Inclusione di un valore ID versione aggiornato con il `id=` assicura che le voci della cache precedenti non siano più accessibili.

Nella tabella seguente sono elencate le stringhe dell&#39;identificatore di versione da utilizzare per ogni `req=` tipo:

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
   <td> <p> mappa </p> </td> 
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

`req=` i tipi non elencati sopra hanno un TTL breve ( `attribute::NonImgExpiration`) o le loro risposte non sono per nulla memorizzabili in cache; non c’è alcun vantaggio nell’includere `id=` con tali richieste.

## Proprietà {#section-62e973d0d5884abebbb0679f9278ae2c}

Attributo della richiesta. Facoltativo. Sempre ignorato dal server.

## Predefinito {#section-96136720c82842c89505347ec39e6024}

Nessuno.

## Esempio {#section-a5fb871e0ec8485c91c4fca78895d17f}

Vedi la descrizione di [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) ad esempio l’utilizzo.

## Vedi anche {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalogo::scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
