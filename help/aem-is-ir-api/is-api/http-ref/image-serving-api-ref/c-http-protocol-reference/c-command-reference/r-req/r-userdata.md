---
description: Dati utente dal catalogo immagini. Restituisce i dati utente per la voce del catalogo immagini specificata nel percorso url.
seo-description: Dati utente dal catalogo immagini. Restituisce i dati utente per la voce del catalogo immagini specificata nel percorso url.
seo-title: userdata
solution: Experience Manager
title: userdata
topic: Scene7 Image Serving - Image Rendering API
uuid: 7a34adad-f1b6-45a7-94fe-1407845710e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# userdata{#userdata}

Dati utente dal catalogo immagini. Restituisce i dati utente per la voce del catalogo immagini specificata nel percorso url.

`req=userdata[,text|{xml[, *`encoding`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encoding</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Il contenuto di `catalog::UserData` viene restituito. Quando si specifica il formato &#39;text&#39;, tutte le istanze di `??` in `catalog::UserData`vengono sostituite da terminatori di riga e alla fine viene aggiunto un terminatore di riga singolo (CR/LF). Se il percorso dell’URL non corrisponde a una voce di catalogo valida, la risposta sarà costituita solo da un terminatore di riga singolo. Quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39;, viene applicata la formattazione appropriata.

Altri comandi nella stringa di richiesta vengono ignorati.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

>[!NOTE]
>
>Il carattere due punti non è consentito nei nomi delle chiavi delle proprietà userdata.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
