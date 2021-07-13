---
description: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`numero`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Abilita, limita o disabilita l'ottimizzazione per i dispositivi in cui <span class="codeph"> devicePixelRatio</span> è maggiore di <span class="codeph"> 1</span>, ovvero per i dispositivi con visualizzazione ad alta densità come iPhone4 e dispositivi simili. Se attivo, il componente limita le dimensioni della richiesta di immagine IS come se il dispositivo avesse solo un rapporto di pixel di <span class="codeph"> 1</span> e in questo modo riducesse la larghezza di banda. </p> <p>Vedi l'esempio seguente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numero</span> </span> </p> </td> 
   <td colname="col2"> <p> Se si utilizza l'impostazione del limite, il componente consente un'elevata densità di pixel solo fino al limite specificato. </p> <p>Vedi l'esempio seguente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

Di seguito sono riportati i risultati previsti quando utilizzi questo attributo di configurazione con il visualizzatore e la dimensione del visualizzatore è 1000 x 1000:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Se la variabile impostata è uguale a </p> </th> 
   <th colname="col2" class="entry"> <p>Risultato </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sempre</span> </p> </td> 
   <td colname="col2"> <p>La densità dei pixel dello schermo/dispositivo viene sempre presa in considerazione. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Se la densità dei pixel dello schermo = 1, allora l'immagine richiesta è 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Se la densità dei pixel dello schermo = 1,5, l'immagine richiesta è 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Se la densità dei pixel dello schermo è 2, allora l'immagine richiesta è 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mai</span> </p> </td> 
   <td colname="col2"> <p>Utilizza sempre una densità di pixel di 1 e ignora la capacità HD del dispositivo. Pertanto, l'immagine richiesta è sempre 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> limite&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>La densità di pixel di un dispositivo viene richiesta e distribuita solo se l'immagine risultante è al di sotto del limite specificato. </p> <p>Il numero limite si applica alla dimensione larghezza o altezza. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Se il numero limite è 1600 e la densità dei pixel è 1,5, viene servita l'immagine 1500 x 1500. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Se il numero limite è 1600 e la densità dei pixel è 2, allora l'immagine 1000 x 1000 viene servita perché l'immagine 2000 x 2000 supera il limite. </p> </li> 
     </ul> </p> <p> <b>Procedure consigliate</b>: Il numero limite deve funzionare insieme all'impostazione aziendale per le dimensioni massime dell'immagine. Pertanto, imposta il numero limite su uguale all'impostazione della dimensione massima dell'immagine aziendale. </p> </td> 
  </tr> 
 </tbody> 
</table>
