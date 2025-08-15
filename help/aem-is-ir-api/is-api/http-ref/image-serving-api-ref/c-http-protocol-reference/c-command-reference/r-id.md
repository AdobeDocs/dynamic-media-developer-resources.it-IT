---
title: Id
description: Versione Immagine/metadati. Quando si lavora con contenuto che cambiano frequentemente, i server in reti caching come Akamai, cache browser e cache server proxy aziendali potrebbero store risposte Immagine Serving che potrebbero non essere aggiornate per periodi di tempo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Id{#id}

Versione Immagine/metadati. Quando si lavora con contenuto che cambiano frequentemente, i server in reti caching come Akamai, cache browser e cache server proxy aziendali potrebbero store risposte Immagine Serving che potrebbero non essere aggiornate per periodi di tempo.

` id= *`Val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Val </span> </span> </p> </td> 
  <td class="stentry"> <p>Versione stringa. </p> </td> 
 </tr> 
</table>

Immagine Serving include un meccanismo controllo delle versioni che consente di ridurre la possibilità che una voce della cache obsoleta venga utilizzata da un applicazione. Questo meccanismo prevede l&#39;utilizzo `req=props` per ottenere stringhe identificativa di versione per i dati e i metadati dell&#39;immagine (ad esempio la mappa immagine o i dati di zoom destinazione). La stringa dell&#39;identificatore della versione viene quindi aggiunta alle richieste di Immagine Serving memorizzabili in cache con il `id=` comando.

Quando un&#39;immagine sorgente o un metadati cambia, cambia anche il valore dell&#39;ID versione corrispondente. L&#39;inclusione di un valore ID versione aggiornato con il `id=` comando assicura che non sia più possibile accedere alle vecchie voci della cache.

Nella tabella seguente sono elencate le stringhe identificatore di versione da utilizzare per ogni `req=` tipo:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> identificatore della versione da req=props</b> </th> 
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
   <td> <p> Obiettivi </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> TMB </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Dati utente </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> XMP </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` i tipi non elencati sopra hanno un TTL breve ( `attribute::NonImgExpiration`) o le loro risposte non sono affatto memorizzabili nella cache; non vi è alcun vantaggio nell&#39;includere `id=` tali richieste.

## Proprietà {#section-62e973d0d5884abebbb0679f9278ae2c}

Attributo request. Opzionale. Sempre ignorato dal server.

## Predefinito {#section-96136720c82842c89505347ec39e6024}

Nessuno.

## Esempio {#section-a5fb871e0ec8485c91c4fca78895d17f}

Vedi la descrizione di [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) per esempio di utilizzo.

## Vedi anche {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
