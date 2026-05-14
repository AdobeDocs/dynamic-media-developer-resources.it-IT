---
title: PageView.transition
description: PageView.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: aa12a210-88d9-4b96-b598-6967496ac668
TQID: 'https://experienceleague.adobe.com/zsCMR3hoGnEbFG1wapFyvB1oKROPcgP9yifLH-wtwPQ'
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

# PageView.transition{#pageview-transition}

` [PageView.|<containerId>_pageView.]transition= *`ora`*[, *`andamento`*]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> volta</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi impiegato dall'animazione per un'azione di incremento di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> andamento</span></span> </p> </td> 
   <td colname="col2"> <p> Crea un'illusione di accelerazione o decelerazione che rende la transizione più naturale. È possibile impostare l'andamento in uno dei seguenti modi: </p> <p> 
     <ul id="ul_DA0D1CF2F2484410BFCCACA86661702E"> 
      <li id="li_93A2D53A53314D9594CEDC9EB20381D4">0 (automatico) </li> 
      <li id="li_AD6A1F03DE544959BC4AA0DD97494F8C"> 1 (lineare) </li> 
      <li id="li_816A3CE796E3415B9650DDA204412A6A"> 2 (quadratico) </li> 
      <li id="li_EF00BF6CA2AA48FEB54015FFBA9F8DD4"> 3 (cubico) </li> 
      <li id="li_F3CB7F0821AF489C84A0CA155F5031A2"> 4 (quartico) </li> 
      <li id="li_F5B844DAF4CC453CA58BF09A660D139F"> 5 (quintico) </li> 
     </ul> </p> <p>La modalità automatica utilizza sempre una transizione lineare quando lo zoom elastico è disattivato (impostazione predefinita). In caso contrario, si adatta a una delle altre funzioni di andamento in base al tempo di transizione. In altre parole, più breve è il tempo di transizione, maggiore è la funzione di andamento utilizzata per accelerare l'effetto di accelerazione o decelerazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-ebfd9162c8504666bf0e4485bf3b1383}

Facoltativo.

## Predefinito {#section-9f91ce6567384ab691e4d4f8a7015455}

`0.5,0`

## Esempio {#section-cb6b8793ee9946b8bf1cfddab8612db5}

`transition=2,2`
