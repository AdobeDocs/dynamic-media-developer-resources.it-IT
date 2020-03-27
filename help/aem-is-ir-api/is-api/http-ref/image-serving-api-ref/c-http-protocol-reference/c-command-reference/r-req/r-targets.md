---
description: Esegue lo zoom dei dati delle destinazioni dal catalogo immagini. Restituisce i dati di destinazione di zoom per la voce del catalogo immagini specificata nel percorso URL.
seo-description: Esegue lo zoom dei dati delle destinazioni dal catalogo immagini. Restituisce i dati di destinazione di zoom per la voce del catalogo immagini specificata nel percorso URL.
seo-title: target
solution: Experience Manager
title: target
topic: Scene7 Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# targets{#targets}

Esegue lo zoom dei dati delle destinazioni dal catalogo immagini. Restituisce i dati di destinazione di zoom per la voce del catalogo immagini specificata nel percorso URL.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

Il contenuto di `catalog::Targets` viene restituito. Quando viene richiesto il formato &#39;text&#39;, tutte le istanze di `??` in `catalog::Targets` vengono sostituite da terminatori di riga e alla fine viene aggiunto un terminatore di riga singolo ( `CR/LF`). Se il percorso dell’URL non corrisponde a una voce di catalogo valida, la risposta sarà costituita solo da un terminatore di riga singolo. Quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39;, viene applicata la formattazione appropriata.

Altri comandi nella stringa di richiesta vengono ignorati.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
