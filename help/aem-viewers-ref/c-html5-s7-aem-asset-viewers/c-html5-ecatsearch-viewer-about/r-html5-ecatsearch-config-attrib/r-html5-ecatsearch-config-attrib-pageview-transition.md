---
description: PageView.transition
solution: Experience Manager
title: PageView.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# PageView.transition{#pageview-transition}

[!DNL `[PageView.|<containerId>_pageView.]transition= *``*[, *`temporizzazione`*]`]

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> time</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tempo in secondi necessario all'animazione per un singolo passaggio di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> allentamento</span></span> </p> </td> 
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

## Proprietà {#section-ebfd9162c8504666bf0e4485bf3b1383}

Facoltativo.

## Predefinito {#section-9f91ce6567384ab691e4d4f8a7015455}

[!DNL `0.5,0`]

## Esempio {#section-cb6b8793ee9946b8bf1cfddab8612db5}

[!DNL `transition=2,2`]
