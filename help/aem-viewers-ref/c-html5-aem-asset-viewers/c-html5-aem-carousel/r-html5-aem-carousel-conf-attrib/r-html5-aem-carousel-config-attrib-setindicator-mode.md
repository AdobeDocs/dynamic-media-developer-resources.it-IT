---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
topic: Dynamic media
uuid: cfb549c2-e0cf-46c3-b5b7-219c8c1bee94
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 6%

---


# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> Configura lo stile di rendering dell'indicatore del set. </p> <p>Se è impostato su <span class="codeph"> dotted</span>, il componente visualizza indicatori identici per tutte le pagine. </p> <p>Se impostato su <span class="codeph"> numeric</span>, inserisce un numero di pagina basato su 1 all'interno di ciascun elemento indicatore. </p> <p>La modalità di funzionamento <span class="codeph"> numeric</span> non è supportata sui dispositivi in grado di effettuare l'input tocco. Il componente utilizza invece <span class="codeph"> dotted</span> su tali dispositivi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
