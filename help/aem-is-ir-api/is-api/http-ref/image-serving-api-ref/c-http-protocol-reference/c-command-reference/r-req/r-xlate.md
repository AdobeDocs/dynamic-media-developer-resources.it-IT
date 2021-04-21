---
description: Versioni disponibili specifiche per le impostazioni internazionali. Restituisce un elenco delle versioni disponibili specifiche per le impostazioni internazionali dell’ID catalogo specificato nel percorso della richiesta.
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 13%

---


# xlate{#xlate}

Versioni disponibili specifiche per le impostazioni internazionali. Restituisce un elenco delle versioni disponibili specifiche per le impostazioni internazionali dell’ID catalogo specificato nel percorso della richiesta.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

Consulta [Traduzione ID oggetto](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

Ad esempio:

`xlate.translatedIds=image,image_fr,image_de`

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
