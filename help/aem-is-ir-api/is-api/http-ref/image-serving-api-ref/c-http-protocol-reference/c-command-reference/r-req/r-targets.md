---
description: Effettua lo zoom dei dati di destinazione dal catalogo immagini. Restituisce i dati di destinazione di zoom per la voce del catalogo immagini specificata nel percorso URL.
solution: Experience Manager
title: target
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 7%

---

# target{#targets}

Effettua lo zoom dei dati di destinazione dal catalogo immagini. Restituisce i dati di destinazione di zoom per la voce del catalogo immagini specificata nel percorso URL.

`req=targets[,text|{xml[, *`codifica`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codifica</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificatore di richiesta univoco. </p></td> 
 </tr> 
</table>

Il contenuto di `catalog::Targets` vengono restituiti. Quando viene richiesto il formato &#39;text&#39;, tutte le istanze di `??` in `catalog::Targets` sono sostituiti da terminatori di riga e da terminatori di riga singola ( `CR/LF`) viene aggiunto alla fine. Se il percorso URL non viene risolto in una voce di catalogo valida, la risposta è costituita solo da un terminatore a riga singola. Quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39; viene applicata la formattazione appropriata.

Altri comandi nella stringa di richiesta vengono ignorati.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa di `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
