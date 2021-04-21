---
description: Opzioni per il ritaglio automatico delle immagini in base al colore.
solution: Experience Manager
title: OpzioniRitaglioColoreAutomatico
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 7%

---


# Opzioni di ritaglio automatico{#autocolorcropoptions}

Opzioni per il ritaglio automatico delle immagini in base al colore.

Sintassi

## Parametri {#section-0302e9238dbc4704914e938f42c881e6}

<table id="table_F6A0DBA37F704C2097C617A0A6767566"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> corner</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Scelta dell'angolo di ritaglio automatico. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolleranza</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Specifica di corrispondenza del colore. Utilizza: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 per abbinare esattamente i colori. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 per consentire la maggior parte delle differenze di colore. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

