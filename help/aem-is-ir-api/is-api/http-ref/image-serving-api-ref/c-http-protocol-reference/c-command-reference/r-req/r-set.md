---
description: Informazioni sul set di file multimediali.
seo-description: Informazioni sul set di file multimediali.
seo-title: set
solution: Experience Manager
title: set
topic: Scene7 Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# set{#set}

Informazioni sul set di file multimediali.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encoding</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta </p></td> 
 </tr> 
</table>

Restituisce informazioni su immagini, video, campioni e vari metadati associati al catalogo::ImageSet per la voce del catalogo immagini specificata nel percorso URL. Questa risposta è una struttura gerarchica determinata dal tipo di set fornito. Quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39;, viene applicata la formattazione appropriata.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::NonImgExpiration`.

>[!NOTE]
>
>Il carattere due punti non è consentito nelle richieste req=set.

Richieste che supportano il formato di risposta JSON consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
