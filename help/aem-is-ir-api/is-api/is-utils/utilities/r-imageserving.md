---
description: Script di controllo Image Server. Questo script viene utilizzato per avviare, arrestare o riavviare Image Server Supervisore, che a sua volta avvia, arresta o riavvia tutti gli altri componenti Image Server.
seo-description: Script di controllo Image Server. Questo script viene utilizzato per avviare, arrestare o riavviare Image Server Supervisore, che a sua volta avvia, arresta o riavvia tutti gli altri componenti Image Server.
seo-title: ImageServer
solution: Experience Manager
title: ImageServer
topic: Scene7 Image Serving - Image Rendering API
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---


# ImageServing{#imageserving}

Script di controllo Image Server. Questo script viene utilizzato per avviare, arrestare o riavviare Image Server Supervisore, che a sua volta avvia, arresta o riavvia tutti gli altri componenti Image Server.

## Utilizzo {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`command`*`

## Comandi {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Comando </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> start  </span> </p> </td> 
   <td colname="col2"> <p> Avviate il Server Supervisore e tutti gli altri componenti Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Arrestate tutti i componenti Image Server, incluso il server di supervisione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Riavvia </span> </p> </td> 
   <td colname="col2"> <p>Riavviate tutti i componenti Image Server, incluso il server di sorveglianza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riavvio { ps | is | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Riavvia Tomcat/Platform Server, Image Server o SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Restituisce informazioni sull’utilizzo del tempo di attività e della memoria corrente per Image Server, Tomcat/Platform Server e SVGserver, oppure lo stato solo per il server specificato; se il Server Supervisore non è in esecuzione, viene restituito un messaggio informativo. </p> </td> 
  </tr> 
 </tbody> 
</table>

