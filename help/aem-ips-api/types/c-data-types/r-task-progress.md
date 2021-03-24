---
description: Informazioni sull’avanzamento dell’attività.
solution: Experience Manager
title: TaskProgress
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# TaskProgress{#taskprogress}

Informazioni sull’avanzamento dell’attività.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Descrizione del tipo di attività. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessed</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Numero di elementi dell'attività già elaborati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Numero di elementi dell'attività in corso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numPending</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Numero di elementi dell'attività in sospeso (non ancora elaborati). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progresso</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> % avanzamento (intervallo 0,0 - 1,0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Messaggio di avanzamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Ora dell’ultimo aggiornamento delle informazioni sull’avanzamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Matrice di elementi dell'attività. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">I valori includono: 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Sconosciuto</span>: Quando l'attività controlla le transizioni tra stati. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Nuovo</span>: Il monitoraggio attività è stato creato ma non ha ancora accettato le attività. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Elaborazione</span>: Monitoraggio attività sta elaborando attivamente le attività. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Arresto</span>: Il monitoraggio attività sta arrestando un processo a causa di una richiesta di arresto del processo. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Fatto</span>: I processi assegnati ai processi di monitoraggio attività sono stati completati. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Non riuscito</span>: Indica un errore irreversibile. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

