---
description: SpinView.transition
solution: Experience Manager
title: SpinView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---


# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *``*[, *`temporizzazione`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi necessario all'animazione per un singolo passaggio di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> allentamento</span></span> </p> </td> 
   <td colname="col2"> <p> Crea un'illusione di accelerazione o decelerazione che rende la transizione più naturale. È possibile impostare l'andamento su una delle seguenti opzioni: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (auto) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (lineare) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadratico) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cubico) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (quartico) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (chintico) </li> 
     </ul> </p> <p>La modalità automatica utilizza sempre la transizione lineare quando lo zoom elastico è disattivato (impostazione predefinita). In caso contrario, si adatta a una delle altre funzioni di allentamento in base al tempo di transizione. Cioè, più breve è il tempo di transizione più alta è la funzione di allentamento utilizzato per accelerare l'effetto di accelerazione o decelerazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
