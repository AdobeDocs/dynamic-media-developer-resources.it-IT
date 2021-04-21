---
description: Controllo della cache. Consente di disattivare selettivamente la memorizzazione in cache lato client (browser, server proxy, sistemi di memorizzazione in cache di rete) e la memorizzazione in cache nella cache interna di Platform Server.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# cache{#cache}

Controllo della cache. Consente di disattivare selettivamente la memorizzazione in cache lato client (browser, server proxy, sistemi di memorizzazione in cache di rete) e la memorizzazione in cache nella cache interna di Platform Server.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>su | disattivato | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>su | disattivato </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>su | disattivato </p></td> 
 </tr> 
</table>

Se viene specificato un solo valore *`cacheControl`*, questo viene applicato sia alle cache client che a quelle server.

La parola chiave &#39; `validate`&#39; consente di aggiornare le voci della cache del server dopo la modifica dei file di texture o vignette, senza dover attendere che la voce della cache scada automaticamente. La memorizzazione in cache del client non è interessata da questo comando.

Se specificato in una richiesta nidificata, `cache=on` abilita la memorizzazione in cache persistente lato server dell&#39;immagine generata dalla richiesta nidificata. Occorre prestare attenzione ad abilitare il caching per le richieste nidificate solo quando ci si aspetta che la stessa richiesta nidificata venga richiamata ripetutamente con esattamente gli stessi parametri.

## Proprietà {#section-0dcbd62e1122400e8c347f408f2d937e}

Può verificarsi in qualsiasi punto della richiesta. Ignorato quando la richiesta non restituisce un&#39;immagine di risposta. *`clientControl`* viene ignorato quando la memorizzazione in cache lato client viene disattivata dal catalogo dei materiali (se  `attribute::Expiration` presenta un valore negativo). *`serverControl`* viene ignorato se la memorizzazione in cache del server è disabilitata (  `PlatformServer::cache.enable`).

## Predefinito {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` per richieste HTTP,  `cache=off` per richieste nidificate/incorporate.

## Consultate anche {#section-2f5853751dab49579e97418fa766bdf9}

[catalogo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
