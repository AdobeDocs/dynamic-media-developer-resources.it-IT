---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`temporizzazione`*]`

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi necessario all'animazione per un singolo passaggio di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> allentamento</span></span> </p> </td> 
   <td colname="col2"> <p> Crea un'illusione di accelerazione o decelerazione che rende la transizione più naturale. È possibile impostare l'andamento su una delle seguenti opzioni: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (auto) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (lineare) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratico) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubico) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartico) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (chintico) </li> 
     </ul> </p> <p>La modalità automatica utilizza sempre la transizione lineare quando lo zoom elastico è disattivato (impostazione predefinita). In caso contrario, si adatta a una delle altre funzioni di allentamento in base al tempo di transizione. Cioè, più breve è il tempo di transizione più alta è la funzione di allentamento utilizzato per accelerare l'effetto di accelerazione o decelerazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`0.5,0`

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`transition=2,2`
