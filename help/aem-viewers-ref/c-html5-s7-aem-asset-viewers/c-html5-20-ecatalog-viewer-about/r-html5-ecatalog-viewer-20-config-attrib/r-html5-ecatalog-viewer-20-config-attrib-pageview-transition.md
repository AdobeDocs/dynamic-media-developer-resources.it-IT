---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
topic: Dynamic media
uuid: f84da456-ac02-4037-b1fd-7440823eb1ef
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *``*[, *`temporizzazione`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi durante il quale l'animazione per un singolo passaggio di zoom viene eseguita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> lenitivo</span></span> </p> </td> 
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

## Proprietà {#section-ebfd9162c8504666bf0e4485bf3b1383}

Facoltativo.

## Predefinito {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## Esempio {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
