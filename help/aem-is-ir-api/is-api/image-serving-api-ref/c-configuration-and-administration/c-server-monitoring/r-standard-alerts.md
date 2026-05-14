---
description: Gli avvisi standard vengono inviati con un messaggio e-mail consolidato alla fine dell’intervallo di calcolo della media configurato.
solution: Experience Manager
title: Avvisi standard
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
TQID: 'https://experienceleague.adobe.com/EJzmjshgrIk8hpvZvljpsWTHSI-mG67UNAg2NVjBcZg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 0%

---

# Avvisi standard{#standard-alerts}

Gli avvisi standard vengono inviati con un messaggio e-mail consolidato alla fine dell’intervallo di calcolo della media configurato.

Nella tabella seguente vengono descritti i tipi di avvisi standard.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Tipo avviso</b> </th> 
   <th class="entry"> <b>ID titolo</b> </th> 
   <th class="entry"> <b>Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Richiesta bloccata </p> </td> 
   <td> <p>Blocca </p> </td> 
   <td> <p>Inviata quando una richiesta non restituisce una risposta al client entro la soglia specificata. Può essere indicativo di richieste bloccate, che possono causare l’esaurimento del pool di thread Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Concorrenza elevata </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Emesso quando il numero di richieste elaborate contemporaneamente (la <i>sovrapposizione</i>) supera la soglia specificata. Può indicare una condizione di sovraccarico del server. </td> 
  </tr> 
  <tr> 
   <td> <p>Traffico minimo </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Generato quando il tasso di richiesta complessivo scende al di sotto della soglia specificata. In genere indica un problema di comunicazione con il server (ad esempio, quando un server viene disconnesso). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Frequenza errori </p> </td> 
   <td> <p>Errore </p> </td> 
   <td> <p>Emesso quando il tasso medio di risposte di errore HTTP durante l’intervallo di campionamento supera la soglia specificata. Può essere indicativo di problemi di configurazione, immagini mancanti, programmazione di siti Web o errori di database. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tempo di risposta </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Inviato quando il tempo medio di elaborazione delle richieste durante l’intervallo di campionamento supera la soglia specificata. In genere indica una condizione di sovraccarico temporanea o persistente del server o del sistema di archiviazione delle immagini back-end. </p> <p>Le risposte di errore non vengono considerate nel calcolo del tempo medio di risposta. </p> </td> 
  </tr> 
 </tbody> 
</table>
