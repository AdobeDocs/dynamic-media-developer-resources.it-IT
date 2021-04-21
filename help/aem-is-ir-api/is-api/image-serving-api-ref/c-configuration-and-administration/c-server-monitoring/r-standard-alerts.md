---
description: Gli avvisi standard vengono inviati con un messaggio e-mail consolidato al termine dell’intervallo di media configurato.
solution: Experience Manager
title: Avvisi standard
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# Avvisi standard{#standard-alerts}

Gli avvisi standard vengono inviati con un messaggio e-mail consolidato al termine dell’intervallo di media configurato.

La tabella seguente descrive ogni tipo di avviso standard.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Tipo di avviso</b> </th> 
   <th class="entry"> <b>Id Titolo</b> </th> 
   <th class="entry"> <b>Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Richiesta bloccata </p> </td> 
   <td> <p>Blocca </p> </td> 
   <td> <p>Inviato quando una richiesta non riesce a restituire una risposta al client entro la soglia specificata. Può essere indicativo delle richieste Hung, che possono causare l'implementazione del pool di thread Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alta concorrenza </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Inviato quando il numero di richieste elaborate contemporaneamente (la <i>sovrapposizione</i>) supera la soglia specificata. Può essere indicativo di una condizione di sovraccarico del server. </td> 
  </tr> 
  <tr> 
   <td> <p>Traffico minimo </p> </td> 
   <td> <p>Traccia </p> </td> 
   <td> <p>Generato quando il tasso di richiesta complessivo scende al di sotto della soglia specificata. In genere indica un problema di comunicazione del server (ad esempio quando un server viene scollegato). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Frequenza errori </p> </td> 
   <td> <p>Errore </p> </td> 
   <td> <p>Inviato quando la frequenza media delle risposte agli errori HTTP durante l’intervallo di campionamento supera la soglia specificata. Può essere indicativo di problemi di configurazione, immagini mancanti o errori di programmazione o database del sito web. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tempo di risposta </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Inviato quando il tempo medio di elaborazione della richiesta durante l’intervallo di campionamento cresce al di sopra della soglia specificata. In genere indica una condizione di sovraccarico temporaneo o persistente del server o del sistema di archiviazione delle immagini di backend. </p> <p>Le risposte agli errori non vengono prese in considerazione quando si calcola il tempo medio di risposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

