---
description: Informazioni sul set di file multimediali.
solution: Experience Manager
title: set
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 9%

---


# set{#set}

Informazioni sul set di file multimediali.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encoding</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta </p></td> 
 </tr> 
</table>

Restituisce informazioni su immagini, video, campioni e vari metadati associati al catalogo::ImageSet per la voce del catalogo immagini specificata nel percorso URL. Questa risposta è una struttura gerarchica determinata dal tipo di set fornito. La formattazione appropriata viene applicata quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39;.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::NonImgExpiration`.

>[!NOTE]
>
>Il carattere due punti non è consentito nelle richieste req=set.

Le richieste che supportano il formato di risposta JSON ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
