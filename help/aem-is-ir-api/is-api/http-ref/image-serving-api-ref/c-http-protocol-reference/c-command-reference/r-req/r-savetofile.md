---
description: Salva l’immagine nel file.
seo-description: Salva l’immagine nel file.
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveToFile{#savetofile}

Salva l’immagine nel file.

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
   <td> <p>Ora di creazione del file (numero di millisecondi trascorsi a partire da mezzanotte, 1 gennaio 1970 UTC/GMT). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelTotal</span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Numero di pixel nell’immagine salvata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> fatto</span> in caso di esito positivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Restituisce lo stato di risposta HTTP 200 in caso di esito positivo e 403 in caso di esito negativo o di timeout della richiesta. La risposta ha un tipo MIME `text/plain` e non è memorizzabile nella cache.

Il salvataggio importante nei file deve essere abilitato specificando il percorso di una cartella scrivibile esistente in `attribute::SavePath`. `saveToFile=` non riesce se `attribute::SavePath` è vuoto.

*`file`* è obbligatorio e deve essere un percorso relativo combinato con `attribute::SavePath`. Image Server non crea cartelle. La cartella di destinazione deve esistere sul server e disporre delle autorizzazioni appropriate per la creazione dei file da parte di Image Server.

`timeout=` è facoltativo. Il timeout predefinito è 60.000 msec, o qualsiasi valore configurato con `PS::SaveTimeout`.
