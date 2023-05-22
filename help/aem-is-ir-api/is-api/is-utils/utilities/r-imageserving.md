---
description: Script di controllo Image Server. Questo script viene utilizzato per avviare, arrestare o riavviare Image Server Supervisor, che a sua volta avvia, arresta o riavvia tutti gli altri componenti di Image Server.
solution: Experience Manager
title: ImageServer
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 1%

---

# ImageServer{#imageserving}

Script di controllo Image Server. Questo script viene utilizzato per avviare, arrestare o riavviare Image Server Supervisor, che a sua volta avvia, arresta o riavvia tutti gli altri componenti di Image Server.

## Utilizzo {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`comando`*`

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
   <td colname="col1"> <p> <span class="codeph"> inizio </span> </p> </td> 
   <td colname="col2"> <p> Avviare Server Supervisor e tutti gli altri componenti Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop </span> </p> </td> 
   <td colname="col2"> <p> Arresta tutti i componenti Image Server, incluso Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riavvia </span> </p> </td> 
   <td colname="col2"> <p>Riavvia tutti i componenti Image Server, incluso Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riavvia { ps | è | svg } </span> </p> </td> 
   <td colname="col2"> <p> Riavvia Tomcat/[!DNL Platform Server], il server immagini o SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stato [ ps | è | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Restituisce il tempo di attività e le informazioni sull'utilizzo della memoria corrente per il server immagini, Tomcat/[!DNL Platform Server], e SVGserver o lo stato solo per il server specificato. Se Server Supervisor non è in esecuzione, viene restituito un messaggio informativo. </p> </td> 
  </tr> 
 </tbody> 
</table>
