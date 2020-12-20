---
description: Proprietà dei dati di risposta. Valuta la richiesta corrente come se fosse una richiesta di immagine (req=img), ma invece di restituire l’immagine, il server restituisce le proprietà selezionate dell’immagine di risposta.
seo-description: Proprietà dei dati di risposta. Valuta la richiesta corrente come se fosse una richiesta di immagine (req=img), ma invece di restituire l’immagine, il server restituisce le proprietà selezionate dell’immagine di risposta.
seo-title: prop
solution: Experience Manager
title: prop
topic: Scene7 Image Serving - Image Rendering API
uuid: b9325654-81d6-4f00-bf0a-36650bea6b8d
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 2%

---


# props{#props}

Proprietà dei dati di risposta. Valuta la richiesta corrente come se fosse una richiesta di immagine (req=img), ma invece di restituire l’immagine, il server restituisce le proprietà selezionate dell’immagine di risposta.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p> </td> 
 </tr> 
</table>

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Per una descrizione della sintassi di risposta e del tipo MIME di risposta, vedere [Properties](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9). La risposta HTTP può essere memorizzata nella cache con un TTL basato su `attribute::NonImgExpiration`.

Per le richieste /is/image vengono restituite le seguenti proprietà:

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> Proprietà</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descrizione</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> eccitare </p> </td> 
   <td> <p> Colore di sfondo (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Rispondi all’altezza dell’immagine in pixel </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> True se il profilo ICC è incorporato nell'immagine di risposta. (Vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Nome/descrizione del profilo associato all’immagine di risposta. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Dimensione risposta in pixel, esclusa l’intestazione HTTP; 0 se i dati dell'immagine di risposta non sono stati memorizzati nella cache in precedenza dal server. (Vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 1 se l'immagine di risposta include un canale alfa, 0 in caso contrario. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Il tipo di immagine di risposta può essere <span class="codeph"> CMYK </span>, <span class="codeph"> RGB </span> o <span class="codeph"> BW </span> (per le immagini in scala di grigio). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 se l’immagine di risposta incorpora dei percorsi, 0 in caso contrario. (Vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> Risoluzione di stampa (dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Qualità JPEG. (Vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Mime type per l'immagine di risposta. (Vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Rispondi alla larghezza dell’immagine in pixel. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed  </span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 se l’immagine di risposta incorpora dati xmp, 0 in caso contrario. (Vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Identificatore versione immagine. (Vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Identificatore versione metadati. (Vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

Per le richieste `/is/content` vengono restituite le seguenti proprietà:

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> Proprietà</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descrizione</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> path  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Percorso del file parzialmente risolto. (Vedere <span class="codeph"> static::Path </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Dimensioni del file dell'oggetto in byte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> exit  </span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> static::Scadenza  </span> o ora predefinita in cui vivere </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Data/ora di modifica (da <span class="codeph"> statica::TimeStamp </span> o dal file dell'oggetto) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> static:UserType  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

