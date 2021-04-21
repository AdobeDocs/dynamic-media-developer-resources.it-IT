---
description: SpinView.autospin
solution: Experience Manager
title: SpinView.autospin
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---


# SpinView.autospin{#spinview-autospin}

` [SpinView.|<containerId>_spinView.]maxloadradius=0|1[, *``*][, *``*][, *`durationdirectionspin_number`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Abilita o disabilita l’animazione a rotazione automatica. Per ottenere la migliore esperienza di rotazione automatica, è consigliabile precaricare tutti i fotogrammi impostando <span class="codeph"> maxloadradius</span> su <span class="codeph"> -1</span>. Tieni presente, tuttavia, che ciò comporta un maggiore tempo di caricamento e un maggiore utilizzo della larghezza di banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durata</span></span> </p> </td> 
   <td colname="col2"> <p> Il numero di secondi per un giro completo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> direzione</span></span> </p> </td> 
   <td colname="col2"> <p> La direzione di rotazione che è <span class="codeph"> 0</span> per la rotazione verso est e <span class="codeph"> 1</span> per la rotazione verso ovest. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> spin_number</span></span> </p> </td> 
   <td colname="col2"> <p> Il numero di rotazioni complete effettuate prima dell'arresto dell'autosfera. Il numero è un numero a virgola mobile. Imposta su <span class="codeph"> -1</span> per un giro automatico infinito. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`0,1,1,1`

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`autospin=1,2,-1,1`
