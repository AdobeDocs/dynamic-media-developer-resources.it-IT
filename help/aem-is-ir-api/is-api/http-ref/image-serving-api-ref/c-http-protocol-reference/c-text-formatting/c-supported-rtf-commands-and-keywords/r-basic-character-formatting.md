---
description: Utilizzare i comandi seguenti per la formattazione di base dei caratteri.
seo-description: Utilizzare i comandi seguenti per la formattazione di base dei caratteri.
seo-title: Formattazione dei caratteri di base
solution: Experience Manager
title: Formattazione dei caratteri di base
topic: Scene7 Image Serving - Image Rendering API
uuid: cc8f276a-ebcc-479b-bd86-7ac0dc755f11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 5%

---


# Formattazione caratteri di base{#basic-character-formatting}

Utilizzare i comandi seguenti per la formattazione di base dei caratteri.

<table id="table_65415B84652F4E7497299AD90AE7C191"> 
 <thead> 
  <tr> 
   <th class="entry"> Comando </th> 
   <th class="entry"> Descrizione </th> 
   <th class="entry"> Note </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \plain  </span> </td> 
   <td> <p>Reimposta la formattazione dei caratteri su quella predefinita. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> solo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \f  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Tipo di carattere. </p> </td> 
   <td> <p> <span class="codeph"> \fonttbl  </span> index. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fs  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Dimensione del font. </p> </td> 
   <td> <p>Mezzo punto; il valore predefinito è 24. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cf  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Colore font. </p> </td> 
   <td> <p>Indice basato su 0 in tavola colori. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \b </span> </td> 
   <td> <p>Stile grassetto. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \i  </span> </td> 
   <td> <p>Stile corsivo. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sub  </span> </td> 
   <td> <p>Pedice. </p> </td> 
   <td> <p>Riduce la dimensione del font. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \super  </span> </td> 
   <td> <p>Apice. </p> </td> 
   <td> <p>Riduce la dimensione del font. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <span class="codeph"> \ul  </span> </td> 
   <td> <p>Sottolineato. </p> </td> 
   <td> <p>Image Serving riconosce anche i seguenti comandi di sottolineatura RTF: </p> <p> 
     <ul id="ul_EF2077DD51F94E2E94D8F1FA661F95DE"> 
      <li id="li_F9382148CCCC4A6AB373DD96D28B71EE"> <span class="codeph"> \uld  </span> </li> 
      <li id="li_141276B2082E4AD0A8C7D3BDDADD6EE2"> <span class="codeph"> \uldash  </span> </li> 
      <li id="li_32CE2C69EEFE462FB21F49FF52A65B0B"> <span class="codeph"> \uldashd  </span> </li> 
      <li id="li_DCF3CD4F884845A5A6B84BDD8DB3A572"> <span class="codeph"> \uldashdd  </span> </li> 
      <li id="li_FDEF96CCE14D41BDB878AADCFF73068F"> <span class="codeph"> \uldb  </span> </li> 
      <li id="li_482CCC6F5D8544CCA69DF2A070097ABD"> <span class="codeph"> \ulth  </span> </li> 
      <li id="li_F11C79A6640B4C0684CA5D9733E49F43"> <span class="codeph"> \ulw  </span> </li> 
      <li id="li_84F94D17372B4C0494A9F8AEC951C556"> <span class="codeph"> \ulwave  </span> </li> 
     </ul> </p> <p>Al momento, queste vengono implementate come sottolineatura standard <span class="codeph"> \ul </span>. Tutti gli altri comandi RTF di sottolineatura vengono ignorati. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ulnone  </span> </td> 
   <td> <p>disattivazione sottolineatura </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ul0  </span> </td> 
   <td> <p>disattivazione sottolineatura </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \Maiuscole </span> </td> 
   <td> <p>maiuscolo </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> solo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \scaps  </span> </td> 
   <td> <p>minuscole ("maiuscoletto") </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> solo. </p> </td> 
  </tr> 
 </tbody> 
</table>

