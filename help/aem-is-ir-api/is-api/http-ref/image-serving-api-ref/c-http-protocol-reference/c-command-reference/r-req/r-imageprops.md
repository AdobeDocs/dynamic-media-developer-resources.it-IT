---
description: Proprietà immagine di origine. Restituisce le proprietà selezionate del file immagine o della voce di catalogo specificate nel percorso URL.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 4%

---

# imageprops{#imageprops}

Proprietà immagine di origine. Restituisce le proprietà selezionate del file immagine o della voce di catalogo specificate nel percorso URL.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

La risposta HTTP può essere memorizzata nella cache con TTL basato su `attribute::NonImgExpiration`.

Altri comandi nella stringa di richiesta vengono ignorati.

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

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
   <td> <p> <span class="codeph"> catalogo: </span> ancoraggio del punto di ancoraggio predefinito </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> catalogo: </span> : scadenza o ora predefinita in cui vivere </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Altezza immagine a piena risoluzione in pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> string </p> </td> 
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
   <td> <p> 1 se l'immagine include i dati del percorso Photoshop </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine. embeddedXmpData</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se l'immagine include dati XMP </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 per nessuna maschera, 1 per alfa premoltiplicato, 2 per alfa non premoltiplicato e 3 per un'immagine separata della maschera </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> catalogo: </span> Modificatore o vuoto se non è presente una voce di catalogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> immagine. photoshopPathNames</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Elenco separato da virgole dei nomi di tutti i percorsi Photoshop associati a questa immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Tipo di immagine, può essere 'CMYK', 'RGB' o 'BW' (per immagini in scala di grigi) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> attributo: </span> PostModificatore o vuoto se non è presente una voce di catalogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> risoluzione di stampa predefinita in pixel/pollice </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> <span class="codeph"> catalogo: </span> Risoluzione o risoluzione predefinita dell'oggetto </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Data/ora di modifica (da <span class="codeph"> catalogo::TimeStamp</span> o dal file immagine) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> <span class="codeph"> catalogo::</span> ThumbResor la risoluzione predefinita delle miniature </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalog::</span> ThumbType o il tipo di miniatura predefinito </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Larghezza immagine a piena risoluzione in pixel </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translateId</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> ID catalogo a cui è stato risolto l' <span class="varname"> oggetto</span> specificato nel percorso (consulta <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Traduzione ID oggetto</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
