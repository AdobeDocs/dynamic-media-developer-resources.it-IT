---
title: SpinView.transition
description: SpinView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: fcffe282-65a5-4093-8838-71a64085b387
TQID: 'https://experienceleague.adobe.com/8v0KA79kf8-EGxgxxJ4FfldLCzUh5wAiV0dy4LmcM5A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# SpinView.transition{#spinview-transition}

` [SpinView.|<containerId>_spinView.]transition= *`ora`*[, *`andamento`*]`

<table id="table_5B8094216AE94DC59671E06DB941A366"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> volta</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi impiegato dall'animazione per un'azione di incremento di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> andamento</span></span> </p> </td> 
   <td colname="col2"> <p> Crea un'illusione di accelerazione o decelerazione che rende la transizione più naturale. È possibile impostare l'andamento in uno dei seguenti modi: </p> <p> 
     <ul id="ul_7B9694978D96449AB986AED1CF7F649D"> 
      <li id="li_904CEC8AD5834139A5585EE70ACE9C80">0 (automatico) </li> 
      <li id="li_471D4CD39C10415497B1714B0AD961B9"> 1 (lineare) </li> 
      <li id="li_7A0F9F1186604E75BAA19626A844236A"> 2 (quadratico) </li> 
      <li id="li_B8D4C40D795642AB835925582B707158"> 3 (cubico) </li> 
      <li id="li_2B9F7324BB89455C89C1CAE1BD5BBB65"> 4 (quartico) </li> 
      <li id="li_B94A553B6E844247BE88ECA0A8CEB811"> 5 (quintico) </li> 
     </ul> </p> <p>La modalità automatica utilizza sempre una transizione lineare quando lo zoom elastico è disattivato (impostazione predefinita). In caso contrario, si adatta a una delle altre funzioni di andamento in base al tempo di transizione. In altre parole, più breve è il tempo di transizione, maggiore è la funzione di andamento utilizzata per accelerare l'effetto di accelerazione o decelerazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0.5,0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=2,2`
