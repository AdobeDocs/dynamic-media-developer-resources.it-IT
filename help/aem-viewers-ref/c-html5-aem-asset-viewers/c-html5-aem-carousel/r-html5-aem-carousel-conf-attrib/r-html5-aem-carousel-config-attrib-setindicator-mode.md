---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 4%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numerico|punteggiato</span> </p> </td> 
   <td colname="col2"> <p> Configura lo stile di rendering dell'indicatore impostato. </p> <p>Se è impostato su <span class="codeph"> con punti </span>, il componente riproduce indicatori identici per tutte le pagine. </p> <p>Se è impostato su <span class="codeph"> numerico</span>, inserisce un numero di pagina basato su 1 in ogni elemento indicatore. </p> <p>La modalità operativa <span class="codeph"> numeric</span> non è supportata nei dispositivi con input tocco. Il componente utilizza invece <span class="codeph"> punteggiato</span> su tali dispositivi. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
