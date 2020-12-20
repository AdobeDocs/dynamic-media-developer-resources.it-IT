---
description: Dati mappa immagine.
seo-description: Dati mappa immagine.
seo-title: map
solution: Experience Manager
title: map
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 7%

---


# map{#map}

Dati mappa immagine.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

Restituisce `catalog::Map` senza modifiche quando si esegue una query su una voce di catalogo semplice senza ulteriori comandi specificati (non verrà ridimensionata a `catalog::maxPix`).

Se nella richiesta sono specificati altri comandi, viene restituita una mappa immagine composita derivata dal ridimensionamento, ritaglio, rotazione e sovrapposizione di tutti i comandi `catalog::Map` e/o `map=` inclusi nella richiesta, proprio come accade con i dati immagine `req=img`.

Specificare `text` o omettere il secondo parametro per restituire i dati della mappa immagine sotto forma di una stringa di elemento `HTML <AREA>` con tipo MIME risposta `text/plain`.

Specificate `xml` per formattare la risposta come XML invece di HTML. È possibile specificare la codifica del testo facoltativamente. Il valore predefinito è `UTF-8`.

Restituisce una stringa vuota (o un elemento `<AREA>` vuoto) se non sono stati trovati dati mappa per gli oggetti catalogo specificati e/o se non rimangono elementi `<AREA>` dopo il ritaglio delle immagini.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Vedere [Mappe immagine](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
