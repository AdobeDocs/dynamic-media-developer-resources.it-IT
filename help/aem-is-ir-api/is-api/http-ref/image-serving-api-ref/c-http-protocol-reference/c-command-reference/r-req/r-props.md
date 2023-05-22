---
description: Proprietà dei dati di risposta. Valuta la richiesta corrente come se si trattasse di una richiesta di immagine (req=img), ma invece di restituire l’immagine il server restituisce le proprietà selezionate dell’immagine di risposta.
solution: Experience Manager
title: prop
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9933d1dc-ae16-4d17-80ca-a1068cd73b0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 2%

---

# prop{#props}

Proprietà dei dati di risposta. Valuta la richiesta corrente come se si trattasse di una richiesta di immagine (req=img), ma invece di restituire l’immagine il server restituisce le proprietà selezionate dell’immagine di risposta.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificatore di richiesta univoco. </p> </td> 
 </tr> 
</table>

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa di `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Consulta [Proprietà](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) per una descrizione della sintassi di risposta e del tipo MIME di risposta. La risposta HTTP è memorizzabile in cache con un TTL basato su `attribute::NonImgExpiration`.

Per le richieste /is/image vengono restituite le seguenti proprietà:

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> Proprietà</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descrizione</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc </span> </p> </td> 
   <td> <p> esadecimale </p> </td> 
   <td> <p> Colore di sfondo (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height </span> </p> </td> 
   <td> <p> numero intero </p> </td> 
   <td> <p> Altezza immagine di risposta in pixel </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> True se il profilo ICC è incorporato nell'immagine di risposta. (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= IccEmbed </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile </span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Nome/descrizione del profilo associato all’immagine di risposta. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length </span> </p> </td> 
   <td> <p> numero intero </p> </td> 
   <td> <p> Dimensione della risposta in pixel, esclusa l’intestazione HTTP; 0 se i dati dell’immagine di risposta non sono stati precedentemente memorizzati nella cache dal server. (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 1 se l’immagine di risposta include un canale alfa, 0 in caso contrario. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixType </span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Tipo di immagine di risposta, potrebbe essere <span class="codeph"> CMYK </span>, <span class="codeph"> RGB </span> o <span class="codeph"> BW </span> (per immagini in scala di grigio). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se l’immagine di risposta incorpora qualsiasi percorso, 0 in caso contrario. (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= percorso </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes </span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> Risoluzione di stampa (dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality </span> </p> </td> 
   <td> <p> numero intero </p> </td> 
   <td> <p> Qualità JPEG. (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type </span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Tipo MIME per l’immagine di risposta. (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width </span> </p> </td> 
   <td> <p> numero intero </p> </td> 
   <td> <p> Larghezza immagine di risposta in pixel. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se l’immagine di risposta incorpora i dati xmp, 0 in caso contrario. (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version </span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Identificatore della versione dell’immagine. (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version </span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Identificatore della versione dei metadati. (vedere <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

Le seguenti proprietà vengono restituite per `/is/content` richieste:

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> Proprietà</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descrizione</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> percorso </span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p>Percorso file parzialmente risolto. (vedere <span class="codeph"> statico::Percorso </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Dimensione file oggetto in byte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> scadenza </span> </p> </td> 
   <td> <p> doppio </p> </td> 
   <td> <p> <span class="codeph"> statico::Scadenza </span> o il valore predefinito time to live </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified </span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Data/ora di modifica (da <span class="codeph"> statico::Timestamp </span> o il file oggetto) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType </span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> <span class="codeph"> static::UserType </span> </p> </td> 
  </tr> 
 </tbody> 
</table>
