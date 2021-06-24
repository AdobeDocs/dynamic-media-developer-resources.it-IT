---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,Business Practitioner
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numerico|punteggiato</span> </p> </td> 
   <td colname="col2"> <p> Configura lo stile di rendering dell'indicatore del set. </p> <p>Se è impostato su <span class="codeph"> dotted</span> il componente esegue il rendering di indicatori identici per tutte le pagine. </p> <p>Se impostato su <span class="codeph"> numerico</span>, inserisce un numero di pagina basato su 1 all'interno di ciascun elemento indicatore. </p> <p>La modalità operativa <span class="codeph"> numerica</span> non è supportata per i dispositivi in grado di inviare dati touch. Il componente utilizza invece <span class="codeph"> dotted</span> su tali dispositivi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
