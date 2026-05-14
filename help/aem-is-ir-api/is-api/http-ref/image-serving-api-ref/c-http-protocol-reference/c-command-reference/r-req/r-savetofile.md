---
description: Salva l'immagine su file.
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
TQID: 'https://experienceleague.adobe.com/6JtqM7IKcYInFZ4zyuAIVwOabdXIltB2ZsVZP6pLL4E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 0%

---

# saveToFile{#savetofile}

Salva l&#39;immagine su file.

`req=saveToFile&name= *`file`*[&timeout= *`val`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p> </td> 
  <td class="stentry"> <p>Percorso relativo del file immagine di destinazione. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Valore <span class="varname"></span> </p></td> 
  <td class="stentry"> <p>Intervallo di timeout (millisecondi). </p></td> 
 </tr> 
</table>

Salva l&#39;immagine di risposta in un file sul server anziché restituirla al client.

Al completamento della richiesta di salvataggio, la richiesta restituisce diverse proprietà in formato Java, tra cui:

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> Proprietà <b></b> </th> 
   <th class="entry"> Tipo <b></b> </th> 
   <th class="entry"> Descrizione <b></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> numero intero </p> </td> 
   <td> <p>Ora di creazione del file (numero di millisecondi dalla mezzanotte del 1° gennaio 1970 UTC/GMT ). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelTotal</span> </p> </td> 
   <td> <p> numero intero </p> </td> 
   <td> <p> Numero di pixel nell’immagine salvata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> Stato <span class="codeph"></span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> completato</span> se completato correttamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Restituisce lo stato di risposta HTTP 200 in caso di esito positivo e 403 in caso di esito negativo o timeout della richiesta. La risposta è di tipo MIME `text/plain` e non è memorizzabile in cache.

È necessario abilitare il salvataggio importante in file specificando il percorso di una cartella scrivibile esistente in `attribute::SavePath`. `saveToFile=` non riesce se `attribute::SavePath` è vuoto.

*`file`* è obbligatorio e deve essere un percorso relativo combinato con `attribute::SavePath`. Image Server non crea cartelle. Per poter creare i file, la cartella di destinazione deve esistere sul server e disporre delle autorizzazioni appropriate per Image Server.

`timeout=` è facoltativo. Il timeout predefinito è di 60.000 msec o qualsiasi valore configurato con `PS::SaveTimeout`.
