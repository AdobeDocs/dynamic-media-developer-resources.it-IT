---
description: Script di controllo Image Server. Questo script viene utilizzato per avviare, arrestare o riavviare Image Server Supervisore, che a sua volta avvia, arresta o riavvia tutti gli altri componenti Image Server.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
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
   <td colname="col2"> <p> Avviare il Server Supervisore e tutti gli altri componenti Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Arresta tutti i componenti Image Server, incluso il server di monitoraggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Riavvia </span> </p> </td> 
   <td colname="col2"> <p>Riavvia tutti i componenti di Image Server, incluso il Server Supervisore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riavvia { ps | | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Riavvia Tomcat/Platform Server, Image Server o SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stato [ ps | | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Restituisce informazioni sull'utilizzo della memoria in tempo utile e corrente per Image Server, Tomcat/Platform Server e SVGserver oppure lo stato solo per il server specificato; se non è in esecuzione, viene restituito un messaggio informativo. </p> </td> 
  </tr> 
 </tbody> 
</table>
