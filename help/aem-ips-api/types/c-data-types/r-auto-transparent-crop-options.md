---
description: Opzioni utilizzate per il ritaglio automatico delle immagini in base alla trasparenza.
solution: Experience Manager
title: OpzioniRitaglioTrasparenteAutomatico
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 351f63a4-cc1b-4db9-93df-c21acd02e12a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 6%

---

# [!DNL AutoTransparentCropOptions]{#autotransparentcropoptions}

Opzioni utilizzate per il ritaglio automatico delle immagini in base alla trasparenza.

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
   <td colname="col1"> <span class="codeph"> tolleranza</span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3">Rimuove lo spazio vuoto dai bordi dell'immagine in base alla trasparenza. Usa: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 per far corrispondere esattamente i colori. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 per ottenere il maggior numero di differenze di colore. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>
