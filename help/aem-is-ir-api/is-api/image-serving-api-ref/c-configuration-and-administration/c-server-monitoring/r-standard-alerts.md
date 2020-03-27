---
description: Gli avvisi standard vengono inviati con un messaggio e-mail consolidato al termine dell’intervallo di media configurato.
seo-description: Gli avvisi standard vengono inviati con un messaggio e-mail consolidato al termine dell’intervallo di media configurato.
seo-title: Avvisi standard
solution: Experience Manager
title: Avvisi standard
topic: Scene7 Image Serving - Image Rendering API
uuid: d3294434-a44b-4742-9d77-a6945760d33c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Avvisi standard{#standard-alerts}

Gli avvisi standard vengono inviati con un messaggio e-mail consolidato al termine dell’intervallo di media configurato.

La tabella seguente descrive ogni tipo di avviso standard.

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
   <td> <p>Lock </p> </td> 
   <td> <p>Inviato quando una richiesta non riesce a restituire una risposta al client entro la soglia specificata. Può essere indicativo delle richieste appese, che possono causare la riduzione del pool di thread Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alta concorrenza </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Inviato quando il numero di richieste elaborate contemporaneamente (la <i>sovrapposizione</i>) supera la soglia specificata. Può essere indicativo di una condizione di sovraccarico del server. </td> 
  </tr> 
  <tr> 
   <td> <p>Traffico minimo </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Generato quando il tasso di richiesta globale scende al di sotto della soglia specificata. In genere indica un problema di comunicazione con il server (ad es. quando un server viene scollegato). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Frequenza errori </p> </td> 
   <td> <p>Errore </p> </td> 
   <td> <p>Emessa quando la frequenza media delle risposte di errore HTTP durante l’intervallo di campionamento supera la soglia specificata. Può essere indicativo di problemi di configurazione, immagini mancanti o errori di programmazione del sito Web o del database. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tempo di risposta </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Inviato quando il tempo medio di elaborazione della richiesta durante l’intervallo di campionamento cresce al di sopra della soglia specificata. In genere indica una condizione di sovraccarico temporaneo o permanente del server o del sistema di memorizzazione delle immagini di back-end. </p> <p>Le risposte agli errori non vengono prese in considerazione quando si calcola il tempo medio di risposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

