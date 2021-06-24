---
description: Salva l'immagine nel file.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 1%

---

# saveToFile{#savetofile}

Salva l&#39;immagine nel file.

`req=saveToFile&name= *``*[&timeout= *`filevale`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>Percorso relativo al file immagine di destinazione. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Intervallo di timeout (millisecondi). </p></td> 
 </tr> 
</table>

Salva l&#39;immagine di risposta in un file sul server anziché restituirla al client.

Al completamento della richiesta di salvataggio, la richiesta restituisce diverse proprietà in formato Java, tra cui:

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Proprietà</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p>Ora di creazione del file (numero di millisecondi trascorsi dalla mezzanotte del 1° gennaio 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelTotal</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Numero di pixel nell’immagine salvata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> </span> doneif riuscito. </p> </td> 
  </tr> 
 </tbody> 
</table>

Restituisce lo stato di risposta HTTP 200 in caso di esito positivo e 403 in caso di errore o timeout della richiesta. La risposta ha il tipo MIME `text/plain` e non è memorizzabile nella cache.

È necessario abilitare il salvataggio importante nei file specificando il percorso di una cartella scrivibile esistente in `attribute::SavePath`. `saveToFile=` non riesce se  `attribute::SavePath` è vuoto.

*`file`* è obbligatorio e deve essere un percorso relativo combinato con  `attribute::SavePath`. Image Server non crea cartelle. La cartella di destinazione deve esistere sul server e disporre delle impostazioni di autorizzazione appropriate per la creazione dei file in Image Server.

`timeout=` è facoltativo. Il timeout predefinito è di 60.000 msec, o qualsiasi valore configurato con `PS::SaveTimeout`.
