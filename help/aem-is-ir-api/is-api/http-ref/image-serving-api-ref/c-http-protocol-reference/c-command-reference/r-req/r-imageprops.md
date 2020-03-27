---
description: Proprietà delle immagini di origine. Restituisce le proprietà selezionate del file immagine o della voce di catalogo specificate nel percorso URL.
seo-description: Proprietà delle immagini di origine. Restituisce le proprietà selezionate del file immagine o della voce di catalogo specificate nel percorso URL.
seo-title: imageprop
solution: Experience Manager
title: imageprop
topic: Scene7 Image Serving - Image Rendering API
uuid: e9bf2780-a520-4fb1-ab4c-40bb799e36a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageprop{#imageprops}

Proprietà delle immagini di origine. Restituisce le proprietà selezionate del file immagine o della voce di catalogo specificate nel percorso URL.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

La risposta HTTP può essere memorizzata nella cache con TTL basato su `attribute::NonImgExpiration`.

Altri comandi nella stringa di richiesta vengono ignorati.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

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
   <td> <p> <span class="codeph"> catalogo:Ancoraggio</span> o punto di ancoraggio predefinito </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expires</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> catalogo::Scadenza</span> o ora predefinita di vita </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Altezza immagine a risoluzione piena in pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Nome/descrizione del profilo associato all'immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 se il profilo associato è incorporato nell'immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 se l'immagine include i dati del percorso di Photoshop </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine. embeddedXmpData</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 se l'immagine include dati XMP </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 per nessuna maschera, 1 per alfa premoltiplicato, 2 per alfa non premoltiplicato e 3 per un'immagine maschera separata </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> catalogo:Modificatore</span> o vuoto se non una voce di catalogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine. photoshopPathNames</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Elenco separato da virgole dei nomi di tutti i percorsi Photoshop associati all’immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Tipo di immagine, può essere 'CMYK', 'RGB' o 'BW' (per le immagini in scala di grigio) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> attribute::PostModificatore</span> o vuoto se non è una voce di catalogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> risoluzione di stampa predefinita in pixel/pollice </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catalogo:Risoluzione</span> o risoluzione predefinita dell'oggetto </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Data/ora di modifica (dal <span class="codeph"> catalogo::TimeStamp</span> o dal file immagine) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catalogo::ThumbRes</span> o risoluzione predefinita delle miniature </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalogo::ThumbType</span> o tipo di miniatura predefinito </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Larghezza immagine a risoluzione piena in pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translateId</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> ID catalogo al quale è stato risolto l' <span class="varname"> oggetto</span> specificato nel percorso (vedere <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Traduzione</a>ID oggetto). </p> </td> 
  </tr> 
 </tbody> 
</table>

