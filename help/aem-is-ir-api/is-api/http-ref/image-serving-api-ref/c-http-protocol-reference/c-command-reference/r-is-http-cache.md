---
title: cache
description: Controllo della cache. Consente di disabilitare in modo selettivo la memorizzazione nella cache lato client (browser, server proxy, sistemi di memorizzazione nella cache di rete) e la memorizzazione nella cache interna [!DNL Platform Server] .
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
TQID: 'https://experienceleague.adobe.com/-52nQ085AMsFuqDNv8JdEtXjwYFtIr3aXfHlrERSDoI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 1%

---

# cache{#cache}

Controllo della cache. Consente di disabilitare in modo selettivo la memorizzazione nella cache lato client (browser, server proxy, sistemi di memorizzazione nella cache di rete) e la memorizzazione nella cache interna di [!DNL Platform Server].

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> attivato|disattivato|convalidato|aggiornamento</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> attivato|disattivato</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> controllo server</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> attivato|disattivato</span> </p></td> 
 </tr> 
</table>

Se viene specificato un solo valore `*`cacheControl`*`, verrà applicato sia alle cache client che a quelle server.

La parola chiave `validate` consente di aggiornare le voci della cache dopo la modifica dei file immagine, senza dover attendere la scadenza automatica della voce della cache. Il caching del client non è interessato da questo comando.

La parola chiave `update` può essere utilizzata per forzare l&#39;aggiornamento delle voci della cache lato server. Ciò è utile dopo che sono state modificate le risorse che non vengono tracciate direttamente dal meccanismo di convalida della cache, ad esempio quando un file di font viene modificato senza modificarne il nome file o l’ID font associato.

Se specificato in una richiesta nidificata, `cache=on` abilita il caching persistente lato server dell&#39;immagine generata dalla richiesta nidificata. È necessario prestare attenzione affinché il caching per le richieste nidificate venga abilitato solo quando si prevede che la stessa richiesta nidificata venga chiamata ripetutamente con esattamente gli stessi parametri.

## Proprietà {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Attributo della richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato quando la richiesta non restituisce un’immagine di risposta. *`clientControl`*viene ignorato quando il caching lato client è disabilitato dal catalogo immagini (se `catalog::Expiration` ha un valore negativo).

Il controllo della cache lato client (solo `on` e `off`) è disponibile anche per le richieste di contenuto statico in [!DNL /is/content/].

## Predefinito {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` per le richieste HTTP, `cache=off` per le richieste nidificate/incorporate, `cache=on` per le richieste di contenuto statico.

## Consultate anche {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalogo::Scadenza](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
