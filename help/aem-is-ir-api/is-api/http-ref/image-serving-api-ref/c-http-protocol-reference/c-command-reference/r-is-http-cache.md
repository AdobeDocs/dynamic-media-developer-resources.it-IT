---
description: Controllo della cache. Consente di disattivare selettivamente la memorizzazione in cache lato client (browser, server proxy, sistemi di memorizzazione in cache di rete) e la memorizzazione in cache nella cache interna di Platform Server.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---


# cache{#cache}

Controllo della cache. Consente di disattivare selettivamente la memorizzazione in cache lato client (browser, server proxy, sistemi di memorizzazione in cache di rete) e la memorizzazione in cache nella cache interna di Platform Server.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

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

Se viene specificato un solo valore `*`cacheControl`*`, questo viene applicato sia alla cache client che al server.

La parola chiave `validate` consente di aggiornare le voci della cache dopo la modifica dei file immagine, senza dover attendere che la voce della cache scada automaticamente. La memorizzazione in cache del client non è interessata da questo comando.

La parola chiave `update` può essere utilizzata per forzare l&#39;aggiornamento delle voci della cache lato server. Questa funzione è utile dopo che sono state modificate le risorse che non vengono tracciate direttamente dal meccanismo di convalida della cache, ad esempio quando un file di font viene modificato senza modificarne il nome o l’ID di font associato.

Se specificato in una richiesta nidificata, `cache=on` abilita la memorizzazione in cache persistente lato server dell&#39;immagine generata dalla richiesta nidificata. Occorre prestare attenzione ad abilitare il caching per le richieste nidificate solo quando ci si aspetta che la stessa richiesta nidificata venga richiamata ripetutamente con esattamente gli stessi parametri.

## Proprietà {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Attributo di richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato quando la richiesta non restituisce un&#39;immagine di risposta. *`clientControl`*viene ignorato quando la memorizzazione in cache lato client è disabilitata dal catalogo immagini (se `catalog::Expiration` ha un valore negativo).

Il controllo della cache lato client ( `on` e `off` solo) è disponibile anche per le richieste di contenuto statico in [!DNL /is/content/].

## Predefinito {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` per le richieste HTTP,  `cache=off` per le richieste nidificate/incorporate,  `cache=on` per le richieste di contenuto statico.

## Consultate anche {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
