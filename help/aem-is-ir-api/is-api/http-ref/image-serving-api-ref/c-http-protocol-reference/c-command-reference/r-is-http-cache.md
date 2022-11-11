---
description: Controllo della cache. Consente di disattivare selettivamente la memorizzazione in cache lato client (browser, server proxy, sistemi di memorizzazione in cache di rete) e la memorizzazione in cache interna [!DNL Platform Server] cache.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# cache{#cache}

Controllo della cache. Consente di disattivare selettivamente la memorizzazione in cache lato client (browser, server proxy, sistemi di memorizzazione in cache di rete) e la memorizzazione in cache interna [!DNL Platform Server] cache.

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

Se solo uno `*`cacheControl`*` viene specificato, viene applicato sia alle cache client che a quelle server.

La `validate` keyword consente di aggiornare le voci della cache dopo la modifica dei file immagine, senza dover attendere che la voce della cache scada automaticamente. La memorizzazione in cache del client non è interessata da questo comando.

La `update` è possibile utilizzare la parola chiave per forzare l&#39;aggiornamento delle voci della cache lato server. Questa funzione è utile dopo che sono state modificate le risorse che non vengono tracciate direttamente dal meccanismo di convalida della cache, ad esempio quando un file di font viene modificato senza modificarne il nome o l’ID di font associato.

Se specificato in una richiesta nidificata, `cache=on` abilita la memorizzazione in cache permanente lato server dell&#39;immagine generata dalla richiesta nidificata. Occorre prestare attenzione ad abilitare il caching per le richieste nidificate solo quando ci si aspetta che la stessa richiesta nidificata venga richiamata ripetutamente con esattamente gli stessi parametri.

## Proprietà {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Attributo di richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato quando la richiesta non restituisce un&#39;immagine di risposta. *`clientControl`*viene ignorato quando la memorizzazione in cache lato client è disattivata dal catalogo immagini (se `catalog::Expiration` ha un valore negativo).

Controllo della cache lato client ( `on` e `off` è disponibile anche per le richieste di contenuto statico in [!DNL /is/content/].

## Predefinito {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` per le richieste HTTP, `cache=off` per le richieste nidificate/incorporate, `cache=on` per richieste di contenuto statico.

## Consultate anche {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
