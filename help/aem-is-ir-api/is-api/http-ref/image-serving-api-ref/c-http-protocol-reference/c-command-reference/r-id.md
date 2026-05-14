---
title: id
description: Versione immagine/metadati. Quando si lavora con contenuti che cambiano frequentemente, i server nelle reti di memorizzazione in cache come Akamai, nelle cache del browser e nelle cache dei server proxy aziendali possono memorizzare le risposte Image Server che potrebbero essere obsolete per periodi di tempo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
TQID: 'https://experienceleague.adobe.com/TPRGzHQ-TxTusgeqo2eLlCG0fNOtmJ1IHIxuUy8bh2I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 267
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

Image Server include un meccanismo di controllo delle versioni che può aiutare a ridurre la possibilità che un’applicazione utilizzi una voce di cache obsoleta. Questo meccanismo comporta l&#39;utilizzo di `req=props` per ottenere stringhe di identificatori di versione per i dati immagine e metadati (ad esempio, mappa immagine o dati di destinazione di zoom). La stringa dell&#39;identificatore di versione viene quindi aggiunta alle richieste di Image Server memorizzabili nella cache con il comando `id=`.

Quando un’immagine sorgente o i metadati cambiano, cambia anche il valore dell’ID versione corrispondente. L&#39;inclusione di un ID di versione aggiornato con il comando `id=` impedisce l&#39;accesso alle voci della cache precedenti.

Nella tabella seguente sono elencate le stringhe dell&#39;identificatore di versione da utilizzare per ogni tipo `req=`:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> richiesta= tipo</b> </th> 
   <th class="entry"> Identificatore di versione <b> da req=props</b> </th> 
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

`req=` tipi non elencati sopra hanno un TTL breve ( `attribute::NonImgExpiration`) o le loro risposte non sono memorizzabili nella cache; non c&#39;è alcun vantaggio nell&#39;includere `id=` con tali richieste.

## Proprietà {#section-62e973d0d5884abebbb0679f9278ae2c}

Attributo della richiesta. Facoltativo. Sempre ignorato dal server.

## Predefinito {#section-96136720c82842c89505347ec39e6024}

Nessuno.

## Esempio {#section-a5fb871e0ec8485c91c4fca78895d17f}

Per informazioni sull&#39;utilizzo, vedere la descrizione di [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3).

## Vedi anche {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
