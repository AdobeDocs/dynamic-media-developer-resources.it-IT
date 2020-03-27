---
description: Controllo cache. Consente di disattivare selettivamente la memorizzazione nella cache lato client (browser, server proxy, sistemi di cache di rete) e la memorizzazione nella cache interna del server della piattaforma.
seo-description: Controllo cache. Consente di disattivare selettivamente la memorizzazione nella cache lato client (browser, server proxy, sistemi di cache di rete) e la memorizzazione nella cache interna del server della piattaforma.
seo-title: cache
solution: Experience Manager
title: cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

Controllo cache. Consente di disattivare selettivamente la memorizzazione nella cache lato client (browser, server proxy, sistemi di cache di rete) e la memorizzazione nella cache interna del server della piattaforma.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on| Off| validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>on| Off </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>on| Off </p></td> 
 </tr> 
</table>

Se viene specificato un solo *`cacheControl`* valore, questo viene applicato sia alle cache client che a quelle del server.

La parola chiave &#39; `validate`&#39; consente di aggiornare le voci della cache del server dopo la modifica dei file di texture o vignettatura, senza dover attendere la scadenza automatica della voce della cache. Il comando non influisce sul caching dei client.

Se specificato in una richiesta nidificata, `cache=on` abilita il caching permanente lato server dell’immagine generata dalla richiesta nidificata. Prestate attenzione a abilitare il caching per le richieste nidificate solo quando è previsto che la stessa richiesta nidificata venga richiamata ripetutamente con gli stessi parametri.

## Proprietà {#section-0dcbd62e1122400e8c347f408f2d937e}

Può verificarsi ovunque nella richiesta. Ignorato quando la richiesta non restituisce un&#39;immagine di risposta. *`clientControl`* viene ignorato quando il caching sul lato client viene disabilitato dal catalogo dei materiali (se `attribute::Expiration` ha un valore negativo). *`serverControl`* viene ignorato se il caching del server è disabilitato ( `PlatformServer::cache.enable`).

## Predefinito {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` per richieste HTTP, `cache=off` per richieste nidificate/incorporate.

## Consultate anche {#section-2f5853751dab49579e97418fa766bdf9}

[catalogo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
