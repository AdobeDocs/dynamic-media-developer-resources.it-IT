---
title: cache
description: Controllo della cache. Consente di disabilitare in modo selettivo il caching lato client (browser, server proxy, sistemi di caching di rete) e il caching interno [!DNL Platform Server] cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# cache{#cache}

Controllo della cache. Consente di disabilitare in modo selettivo il caching lato client (browser, server proxy, sistemi di caching di rete) e il caching interno [!DNL Platform Server] cache.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Se solo uno `*`cacheControl`*` è specificato, viene applicato sia alle cache client che a quelle server.

Il `validate` parola chiave consente di aggiornare le voci della cache dopo la modifica dei file immagine, senza dover attendere la scadenza automatica della voce della cache. Il caching del client non è interessato da questo comando.

Il `update` è possibile utilizzare la parola chiave per forzare l’aggiornamento delle voci della cache lato server. Ciò è utile dopo che sono state modificate le risorse che non vengono tracciate direttamente dal meccanismo di convalida della cache, ad esempio quando un file di font viene modificato senza modificarne il nome file o l’ID font associato.

Se specificato in una richiesta nidificata, `cache=on` abilita il caching persistente lato server dell’immagine generata dalla richiesta nidificata. È necessario prestare attenzione affinché il caching per le richieste nidificate venga abilitato solo quando si prevede che la stessa richiesta nidificata venga chiamata ripetutamente con esattamente gli stessi parametri.

## Proprietà {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Attributo della richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato quando la richiesta non restituisce un’immagine di risposta. *`clientControl`*viene ignorato quando il caching lato client viene disabilitato dal catalogo immagini (se `catalog::Expiration` ha un valore negativo).

Controllo cache lato client ( `on` e `off` solo ) è disponibile anche per le richieste di contenuto statico all’indirizzo [!DNL /is/content/].

## Predefinito {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` per le richieste HTTP, `cache=off` per richieste nidificate/incorporate, `cache=on` per richieste di contenuto statico.

## Consultate anche {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalogo::scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
