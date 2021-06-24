---
description: Lo zoom esegue la destinazione dei dati dal catalogo immagini. Restituisce i dati di destinazione dello zoom per la voce del catalogo immagini specificata nel percorso URL.
solution: Experience Manager
title: target
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 6%

---

# target{#targets}

Lo zoom esegue la destinazione dei dati dal catalogo immagini. Restituisce i dati di destinazione dello zoom per la voce del catalogo immagini specificata nel percorso URL.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificatore univoco della richiesta. </p></td> 
 </tr> 
</table>

Vengono restituiti i contenuti di `catalog::Targets`. Quando viene richiesto il formato &quot;text&quot;, tutte le istanze di `??` in `catalog::Targets` vengono sostituite da terminatori di riga e alla fine viene aggiunto un terminatore di riga singolo ( `CR/LF`). Se il percorso URL non viene risolto in una voce di catalogo valida, la risposta è costituita solo da un terminatore di riga singolo. La formattazione appropriata viene applicata quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39;.

Altri comandi nella stringa di richiesta vengono ignorati.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
