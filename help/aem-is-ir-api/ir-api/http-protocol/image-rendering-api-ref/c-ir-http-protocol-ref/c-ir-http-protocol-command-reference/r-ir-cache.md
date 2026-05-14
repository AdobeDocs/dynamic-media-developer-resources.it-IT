---
title: cache
description: Controllo cache. Consente di disabilitare in modo selettivo la memorizzazione nella cache lato client (browser, server proxy, sistemi di memorizzazione nella cache di rete) e la memorizzazione nella cache interna [!DNL Platform Server] .
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
TQID: 'https://experienceleague.adobe.com/xq-8hE9RB7I-CMb-yguhBcEttxTv6IRRHWzh0lDvn6E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 1%

---

# cache {#cache}

Controllo cache. Consente di disabilitare in modo selettivo il caching lato client (browser, server proxy, sistemi di caching di rete) e il caching nella cache interna di [!DNL Platform Server].

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>il | disattivato | convalida </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>il | disattivato </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> controllo server </span> </p></td> 
  <td class="stentry"> <p>il | disattivato </p></td> 
 </tr> 
</table>

Se viene specificato un solo valore *`cacheControl`*, verrà applicato sia alle cache client che a quelle server.

La parola chiave &#39;`validate`&#39; consente di aggiornare le voci della cache del server dopo la modifica dei file di texture o vignettatura, senza dover attendere la scadenza automatica della voce della cache. Il caching del client non è interessato da questo comando.

Se specificato in una richiesta nidificata, `cache=on` abilita il caching persistente lato server dell&#39;immagine generata dalla richiesta nidificata. Accertati di abilitare il caching per le richieste nidificate solo quando la stessa richiesta nidificata viene chiamata ripetutamente con gli stessi parametri.

## Proprietà {#section-0dcbd62e1122400e8c347f408f2d937e}

Può verificarsi ovunque nella richiesta. Ignorato quando la richiesta non restituisce un’immagine di risposta. La proprietà *`clientControl`* viene ignorata quando il caching lato client è disabilitato dal catalogo dei materiali (se `attribute::Expiration` ha un valore negativo). La proprietà *`serverControl`* viene ignorata se il caching del server è disabilitato ( `PlatformServer::cache.enable`).

## Predefinito {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` Per le richieste HTTP, `cache=off` per le richieste nidificate/incorporate.

## Consultate anche {#section-2f5853751dab49579e97418fa766bdf9}

[catalogo::Scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
