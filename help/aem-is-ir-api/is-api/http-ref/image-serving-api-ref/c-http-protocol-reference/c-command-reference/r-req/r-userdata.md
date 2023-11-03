---
description: Dati utente dal catalogo immagini. Restituisce i dati utente per la voce del catalogo immagini specificata nel percorso dell'URL.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 7%

---

# userdata{#userdata}

Dati utente dal catalogo immagini. Restituisce i dati utente per la voce del catalogo immagini specificata nel percorso dell&#39;URL.

`req=userdata[,text|{xml[, *`codifica`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codifica</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Il contenuto di `catalog::UserData` vengono restituiti. Quando si specifica il formato &#39;text&#39;, tutte le istanze di `??` in `catalog::UserData`sono sostituiti da terminatori di linea e un terminatore a linea singola (CR/LF) è aggiunto alla fine. Se il percorso URL non viene risolto in una voce di catalogo valida, la risposta è costituita solo da un terminatore a riga singola. Quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39; viene applicata la formattazione appropriata.

Altri comandi nella stringa di richiesta vengono ignorati.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

>[!NOTE]
>
>Il carattere due punti non è consentito nei nomi delle chiavi di proprietà userdata.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa di `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
