---
description: Dati mappa immagine.
solution: Experience Manager
title: map
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '213'
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

Restituisce `catalog::Map` senza modifiche quando si esegue una query su una voce di catalogo semplice senza specificare alcun comando aggiuntivo (non verrà ridimensionato in `catalog::maxPix`).

Se nella richiesta sono specificati altri comandi, viene restituita una mappa immagine composita, che viene derivata da ridimensionamento, ritaglio, rotazione e stratificazione di tutti i comandi `catalog::Map` e/o `map=` inclusi nella richiesta, proprio come i dati immagine sarebbero con `req=img`.

Specifica `text` o ometti il secondo parametro per restituire i dati della mappa immagine sotto forma di una stringa di elemento `HTML <AREA>` con tipo MIME di risposta `text/plain`.

Specifica `xml` per formattare la risposta come XML anziché HTML. Facoltativamente, è possibile specificare la codifica del testo. Il valore predefinito è `UTF-8`.

Restituisce una stringa vuota (o un elemento `<AREA>` vuoto) se non sono stati trovati dati mappa per gli oggetti di catalogo specificati e/o se non rimangono elementi `<AREA>` dopo il ritaglio delle immagini.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Consulta [Mappe immagine](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
