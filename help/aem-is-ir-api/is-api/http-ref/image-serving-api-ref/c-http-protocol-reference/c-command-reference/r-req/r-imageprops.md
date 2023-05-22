---
description: Proprietà dell’immagine di origine. Restituisce le proprietà selezionate del file immagine o della voce di catalogo specificata nel percorso URL.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---

# imageprops{#imageprops}

Proprietà dell’immagine di origine. Restituisce le proprietà selezionate del file immagine o della voce di catalogo specificata nel percorso URL.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificatore di richiesta univoco. </p></td> 
 </tr> 
</table>

La risposta HTTP può essere memorizzata nella cache con TTL basato su `attribute::NonImgExpiration`.

Altri comandi nella stringa di richiesta vengono ignorati.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa di `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Vengono restituite le seguenti proprietà:

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> Proprietà</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descrizione</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catalogo::ancoraggio</span> o il punto di ancoraggio predefinito </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> doppio </p> </td> 
   <td> <p> <span class="codeph"> catalogo::scadenza</span> o il valore predefinito time to live </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> numero intero </p> </td> 
   <td> <p>Altezza immagine a piena risoluzione in pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Nome/descrizione del profilo associato a questa immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine. embeddedIccProfile</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se il profilo associato è incorporato nell’immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se l’immagine include i dati del percorso di Photoshop </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine. embeddedXmpData</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se l’immagine include dati XMP </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 per nessuna maschera, 1 per alfa premoltiplicata, 2 per alfa non premoltiplicata e 3 per un'immagine maschera separata </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> <span class="codeph"> catalogo::Modificatore</span> o vuoto se non è una voce di catalogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine. photoshopPathNames</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Elenco separato da virgole dei nomi di tutti i percorsi Photoshop associati a questa immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Il tipo di immagine può essere "CMYK", "RGB" o "BW" (per immagini in scala di grigio) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> <span class="codeph"> attribute::PostModifier</span> o vuoto se non è una voce di catalogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> risoluzione di stampa predefinita in pixel/pollice </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> <span class="codeph"> catalogo::Risoluzione</span> o la risoluzione predefinita dell'oggetto </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p>Data/ora di modifica (da <span class="codeph"> catalogo::Timestamp</span> o il file di immagine) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> <span class="codeph"> catalogo::ThumbRes</span> o la risoluzione predefinita delle miniature </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbType</span> o il tipo di miniatura predefinito </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> numero intero </p> </td> 
   <td> <p> Larghezza immagine a risoluzione massima in pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translationId</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> ID catalogo a cui è associato <span class="varname"> oggetto</span> specificato nel percorso viene risolto (vedere <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Traduzione ID oggetto</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
