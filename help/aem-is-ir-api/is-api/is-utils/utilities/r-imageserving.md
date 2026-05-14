---
description: Script di controllo Image Server. Questo script viene utilizzato per avviare, arrestare o riavviare Image Server Supervisor, che a sua volta avvia, arresta o riavvia tutti gli altri componenti di Image Server.
solution: Experience Manager
title: ImageServer
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
TQID: 'https://experienceleague.adobe.com/KyiS-GblbCE-Q4Exrdz8T1W5thFn9cHellB-1-QYZaw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
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
   <td colname="col1"> <p> <span class="codeph"> interruzione </span> </p> </td> 
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
   <td colname="col1"> <p> Stato <span class="codeph"> [ ps | è | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Restituisce le informazioni sull'utilizzo della memoria corrente e del tempo di attività per Image Server, Tomcat/[!DNL Platform Server] e SVGserver oppure lo stato solo per il server specificato. Se Server Supervisor non è in esecuzione, viene restituito un messaggio informativo. </p> </td> 
  </tr> 
 </tbody> 
</table>
