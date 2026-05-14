---
description: Dati utente dal catalogo immagini. Restituisce i dati utente per la voce del catalogo immagini specificata nel percorso dell'URL.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
TQID: 'https://experienceleague.adobe.com/cLVsaN--jydZTkV6GA92jN1PO8VOFAEZxhSg7F2S9dk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 0%

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

Il contenuto di `catalog::UserData` è stato restituito. Quando si specifica il formato &#39;text&#39;, tutte le istanze di `??` in `catalog::UserData` vengono sostituite da terminatori di riga e un terminatore a riga singola (CR/LF) viene aggiunto alla fine. Se il percorso URL non viene risolto in una voce di catalogo valida, la risposta è costituita solo da un terminatore a riga singola. Quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39; viene applicata la formattazione appropriata.

Altri comandi nella stringa di richiesta vengono ignorati.

La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::Expiration`.

>[!NOTE]
>
>Il carattere due punti non è consentito nei nomi delle chiavi di proprietà userdata.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
