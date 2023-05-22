---
description: Dati mappa immagine.
solution: Experience Manager
title: mappa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 7%

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

Restituisce `catalog::Map` senza modifiche quando si esegue una query su una voce di catalogo semplice senza comandi aggiuntivi specificati (non viene ridimensionata in base a `catalog::maxPix`).

Se nella richiesta sono specificati altri comandi, viene restituita una mappa immagine composita derivata da ridimensionamento, ritaglio, rotazione e sovrapposizione di tutti i comandi `catalog::Map` e/o `map=` comandi inclusi nella richiesta, esattamente come i dati immagine vengono `req=img`.

Specifica `text` o omettere il secondo parametro per restituire i dati della mappa immagine sotto forma di `HTML <AREA>` stringa di elemento con tipo MIME di risposta `text/plain`.

Specifica `xml` per formattare la risposta come XML anziché come HTML. Facoltativamente, è possibile specificare la codifica testo. Il valore predefinito è `UTF-8`.

Restituisce una stringa vuota o vuota `<AREA>` elemento ) se non sono stati trovati dati di mappa per gli oggetti catalogo specificati e/o se no `<AREA>` dopo il ritaglio delle immagini.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa di `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Consulta [Mappe immagine](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
