---
description: Dati del set di immagini dal catalogo immagini. Restituisce i dati del set di immagini per la voce del catalogo immagini specificata nel percorso URL.
seo-description: Dati del set di immagini dal catalogo immagini. Restituisce i dati del set di immagini per la voce del catalogo immagini specificata nel percorso URL.
seo-title: imageset
solution: Experience Manager
title: imageset
topic: Scene7 Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageset{#imageset}

Dati del set di immagini dal catalogo immagini. Restituisce i dati del set di immagini per la voce del catalogo immagini specificata nel percorso URL.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

Il contenuto di `catalog::ImageSet` viene restituito senza ulteriori modifiche (ad eccezione della localizzazione delle stringhe, se applicabile), seguito da un terminatore di riga singolo (CR/LF). Se il percorso dell’URL non corrisponde a una voce di catalogo valida, la risposta sarà costituita solo da un terminatore di riga singolo.

Altri comandi nella stringa di richiesta vengono ignorati. La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::NonImgExpiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
