---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
uuid: cfb549c2-e0cf-46c3-b5b7-219c8c1bee94
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '77'
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
