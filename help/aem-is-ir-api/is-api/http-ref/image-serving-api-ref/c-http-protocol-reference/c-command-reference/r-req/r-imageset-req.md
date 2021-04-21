---
description: Dati del set di immagini dal catalogo immagini. Restituisce i dati del set di immagini per la voce del catalogo immagini specificata nel percorso URL.
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 7%

---


# imageset{#imageset}

Dati del set di immagini dal catalogo immagini. Restituisce i dati del set di immagini per la voce del catalogo immagini specificata nel percorso URL.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

Il contenuto di `catalog::ImageSet` viene restituito senza ulteriori modifiche (ad eccezione della localizzazione delle stringhe, se applicabile), seguito da un terminatore di riga singolo (CR/LF). Se il percorso URL non viene risolto in una voce di catalogo valida, la risposta è costituita solo da un terminatore di riga singolo.

Altri comandi nella stringa di richiesta vengono ignorati. La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::NonImgExpiration`.

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
