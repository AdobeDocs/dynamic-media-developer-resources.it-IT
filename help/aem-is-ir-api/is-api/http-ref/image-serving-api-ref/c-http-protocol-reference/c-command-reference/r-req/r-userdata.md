---
description: Dati utente dal catalogo immagini. Restituisce i dati utente per la voce del catalogo immagini specificata nel percorso URL.
solution: Experience Manager
title: dati utente
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 6%

---

# dati utente{#userdata}

Dati utente dal catalogo immagini. Restituisce i dati utente per la voce del catalogo immagini specificata nel percorso URL.

`req=userdata[,text|{xml[, *`encoding`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encoding</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Vengono restituiti i contenuti di `catalog::UserData`. Quando si specifica il formato &quot;text&quot;, tutte le istanze di `??` in `catalog::UserData`vengono sostituite da terminatori di riga e alla fine viene aggiunto un terminatore di riga singolo (CR/LF). Se il percorso URL non viene risolto in una voce di catalogo valida, la risposta è costituita solo da un terminatore di riga singolo. La formattazione appropriata viene applicata quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39;.

Altri comandi nella stringa di richiesta vengono ignorati.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

>[!NOTE]
>
>Il carattere due punti non è consentito nei nomi delle chiavi delle proprietà dati utente.

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
