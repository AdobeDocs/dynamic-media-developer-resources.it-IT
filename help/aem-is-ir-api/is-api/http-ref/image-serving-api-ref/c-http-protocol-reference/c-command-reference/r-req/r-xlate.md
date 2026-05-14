---
description: Versioni disponibili specifiche per le impostazioni locali. Restituisce un elenco delle versioni disponibili specifiche per le impostazioni internazionali dell'ID catalogo specificato nel percorso della richiesta.
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bf5b3cb7-9792-4eca-a1aa-55aa4089b4d4
TQID: 'https://experienceleague.adobe.com/Ac-h7oQm6fF01YUOz2RQ25dyqLj02shurvkxulWJUHk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 115
ht-degree: 2%

---

# xlate{#xlate}

Versioni disponibili specifiche per le impostazioni locali. Restituisce un elenco delle versioni disponibili specifiche per le impostazioni internazionali dell&#39;ID catalogo specificato nel percorso della richiesta.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificatore di richiesta univoco. </p></td> 
 </tr> 
</table>

Vedi [Traduzione ID oggetto](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Ad esempio:

`xlate.translatedIds=image,image_fr,image_de`

La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::Expiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
