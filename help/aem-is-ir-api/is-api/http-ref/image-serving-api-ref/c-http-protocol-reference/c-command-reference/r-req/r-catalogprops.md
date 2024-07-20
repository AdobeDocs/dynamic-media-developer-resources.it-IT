---
description: Proprietà catalogo immagini. Restituisce gli attributi comuni del catalogo immagini specificato nel percorso della richiesta.
solution: Experience Manager
title: catalogprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28bf68e8-d424-418e-99a7-5298a1d83341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# catalogprops{#catalogprops}

Proprietà catalogo immagini. Restituisce gli attributi comuni del catalogo immagini specificato nel percorso della richiesta.

`req=catalogprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_D1D9183C08834005B482B103CEF2EDA9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificatore di richiesta univoco. </p></td> 
 </tr> 
</table>

Per recuperare le proprietà predefinite del catalogo ( [!DNL default.ini]), omettere l&#39;ID catalogo. La risposta HTTP è memorizzabile in cache con TTL basato su `attribute::NonImgExpiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Vengono restituiti i seguenti valori delle proprietà:

<table id="table_DEC26CBF274945298BA81B5E2E2F331D"> 
 <tbody> 
  <tr> 
   <td> Proprietà <b></b> </td> 
   <td> Tipo <b></b> </td> 
   <td> <b> Attributo catalogo corrispondente</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.bkgColor</span> </p> </td> 
   <td> <p> esadecimale </p> </td> 
   <td> <p> Attributo <span class="codeph">::BkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Catalogo <span class="codeph">::defaultExt</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Attributo <span class="codeph">::DefaultExt</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo.defaultPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> Attributo <span class="codeph">::DefaultPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultThumbPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> Attributo <span class="codeph">::DefaultThumbPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo.scadenza</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> Attributo <span class="codeph">::Scadenza</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.defaultExpiration</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> Attributo <span class="codeph">::DefaultExpiration</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.nonImgExpiration</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> Attributo <span class="codeph">::NonImgExpiration</span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog.fileTime</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Attributo <span class="codeph">::LastModified</span> oppure, se non presente, l'ora dell'ultima modifica del file <span class="varname"> catalog</span><span class="filepath"> .ini</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo.jpegQuality</span> </p> </td> 
   <td> <p> int,bool </p> </td> 
   <td> <p> Attributo <span class="codeph">::JpegQuality</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo.maxPix</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> Attributo <span class="codeph">::MaxPix</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.printResolution</span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Attributo <span class="codeph">::PrintResolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.publishInfo</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Attributo <span class="codeph">::PublishInfo</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.resMode</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> Attributo <span class="codeph">::ResMode</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo.risoluzione</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> Attributo <span class="codeph">::Resolution</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbBkgColor</span> </p> </td> 
   <td> <p> esadecimale </p> </td> 
   <td> <p> Attributo <span class="codeph">::ThumbBkgColor</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo.thumbHorizAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> Attributo <span class="codeph">::ThumbHorizAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbRes</span> </p> </td> 
   <td> <p> reale </p> </td> 
   <td> <p> Attributo <span class="codeph">::ThumbRes</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> Attributo <span class="codeph">::ThumbType</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo.thumbVertAlign</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> Attributo <span class="codeph">::ThumbVertAlign</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalogo::filigrana</span> </p> </td> 
   <td> <p> stringa </p> </td> 
   <td> <p> Attributo <span class="codeph">::Filigrana</span> </p> </td> 
  </tr> 
 </tbody> 
</table>
