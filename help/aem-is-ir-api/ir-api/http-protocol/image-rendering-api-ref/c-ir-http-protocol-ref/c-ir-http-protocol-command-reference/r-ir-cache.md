---
title: cache
description: Controllo cache. Consente di disabilitare in modo selettivo il caching lato client (browser, server proxy, sistemi di caching di rete) e il caching interno [!DNL Platform Server] cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# cache {#cache}

Controllo cache. Consente di disabilitare in modo selettivo il caching lato client (browser, server proxy, sistemi di caching in rete) e il caching interno [!DNL Platform Server] cache.

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
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>il | disattivato </p></td> 
 </tr> 
</table>

Se solo uno *`cacheControl`* è specificato, viene applicato sia alle cache client che a quelle server.

L&#39;&#39; `validate`La parola chiave &#39; consente di aggiornare le voci della cache del server dopo la modifica dei file di texture o vignettatura, senza dover attendere la scadenza automatica della voce della cache. Il caching del client non è interessato da questo comando.

Se specificato in una richiesta nidificata, `cache=on` abilita il caching persistente lato server dell’immagine generata dalla richiesta nidificata. Accertati di abilitare il caching per le richieste nidificate solo quando la stessa richiesta nidificata viene chiamata ripetutamente con gli stessi parametri.

## Proprietà {#section-0dcbd62e1122400e8c347f408f2d937e}

Può verificarsi ovunque nella richiesta. Ignorato quando la richiesta non restituisce un’immagine di risposta. La proprietà *`clientControl`* viene ignorato quando il caching lato client viene disabilitato dal catalogo dei materiali (se `attribute::Expiration` ha un valore negativo). La proprietà *`serverControl`* viene ignorato se il caching del server è disabilitato ( `PlatformServer::cache.enable`).

## Predefinito {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` Per le richieste HTTP: `cache=off` per richieste nidificate/incorporate.

## Consultate anche {#section-2f5853751dab49579e97418fa766bdf9}

[catalogo::scadenza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
