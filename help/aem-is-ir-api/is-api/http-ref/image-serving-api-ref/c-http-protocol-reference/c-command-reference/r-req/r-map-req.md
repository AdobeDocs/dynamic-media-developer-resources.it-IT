---
title: mappa
description: Dati mappa immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# mappa{#map}

Dati mappa immagine.

`req=map[,text|{xml[, *`codifica`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codifica</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificatore di richiesta univoco. </p></td> 
 </tr> 
</table>

Restituisce `catalog::Map` senza modifiche quando viene eseguita una query su una voce di catalogo semplice senza comandi aggiuntivi specificati (non viene ridimensionata a `catalog::maxPix`).

Se nella richiesta sono specificati altri comandi, viene restituita una mappa immagine composita. La mappa immagine composita è derivata dal ridimensionamento, dal ritaglio, dalla rotazione e dal livellamento di tutti i comandi `catalog::Map` e/o `map=` inclusi nella richiesta, proprio come i dati immagine sarebbero con `req=img`.

Specificare `text` o omettere il secondo parametro in modo da poter restituire i dati della mappa immagine sotto forma di una stringa di elemento `HTML <AREA>` con tipo MIME di risposta `text/plain`.

Specificare `xml` in modo da poter formattare la risposta come XML anziché come HTML. Facoltativamente, è possibile specificare la codifica testo. Il valore predefinito è `UTF-8`.

Restituisce una stringa vuota (o un elemento `<AREA>` vuoto) se non sono stati trovati dati di mappa per gli oggetti catalogo specificati e/o se non rimangono elementi `<AREA>` dopo il ritaglio delle immagini.

La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::Expiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Vedi [Mappe immagine](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
