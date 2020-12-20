---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.transition
solution: Experience Manager
title: ZoomView.transition
topic: Dynamic media
uuid: f579397b-a449-42fe-b0a7-f0da65a6a248
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# ZoomView.transition{#zoomview-transition}

` [ZoomView.|<containerId>_zoomView.]transition= *``*[, *`temporizzazione`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> time</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi durante il quale l'animazione per un singolo passaggio di zoom viene eseguita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> lenitivo</span> </span> </p> </td> 
   <td colname="col2"> <p> Crea un'illusione di accelerazione o decelerazione che rende la transizione più naturale. È possibile impostare l'andamento su una delle opzioni seguenti: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automatico) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (lineare) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratico) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubico) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartico) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (chintico) </li> 
     </ul> </p> <p>La modalità Auto utilizza sempre la transizione lineare quando lo zoom elastico è disattivato (impostazione predefinita). In caso contrario, si adatta a una delle altre funzioni di andamento in base al tempo di transizione. In altre parole, più breve è il tempo di transizione maggiore è l'utilizzo della funzione di andamento per accelerare l'effetto di accelerazione o decelerazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`0.5,0`

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`transition=2,2`
