---
description: 'null'
seo-description: 'null'
seo-title: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
topic: Dynamic media
uuid: dcfb202d-6ed8-4cb9-9254-b8dcfe99cd00
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.enableHD{#pageview-enablehd}

` [PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`number`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Abilita, limita o disabilita l’ottimizzazione per i dispositivi in cui <span class="codeph"> devicePixelRatio</span> è maggiore di <span class="codeph"> 1</span>, ovvero per i dispositivi con display ad alta densità come iPhone4 e dispositivi simili. Se attivo, il componente limita le dimensioni della richiesta di immagine IS come se il dispositivo avesse solo un rapporto pixel di <span class="codeph"> 1</span> e in tal modo riducesse la larghezza di banda. </p> <p>Vedere l'esempio seguente </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> number</span></span> </p> </td> 
   <td colname="col2"> <p> Se si utilizza l’impostazione del limite, il componente attiva la densità dei pixel elevati solo fino al limite specificato. </p> <p>Vedere l'esempio seguente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-38b878e38caa439bb462d4fa637afdaa}

Facoltativo.

## Predefinito {#section-50b22de303c1432094530e6583132c02}

`limit,1500`

## Esempio {#section-09433488774245d985acef6c0341ece0}

Di seguito sono riportati i risultati attesi quando usate questo attributo di configurazione con il visualizzatore e la dimensione del visualizzatore è 1000 x 1000:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Se la variabile set è uguale a </p> </th> 
   <th colname="col2" class="entry"> <p>Risultato </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> always</span> </p> </td> 
   <td colname="col2"> <p>La densità in pixel dello schermo o del dispositivo viene sempre presa in considerazione. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Se la densità dei pixel dello schermo = 1, l'immagine richiesta è 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Se la densità dei pixel dello schermo è pari a 1,5, l'immagine richiesta è pari a 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Se la densità dei pixel dello schermo è pari a 2, l'immagine richiesta è pari a 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> never</span> </p> </td> 
   <td colname="col2"> <p>Usa sempre una densità di pixel pari a 1 e ignora la capacità HD del dispositivo. Pertanto, l’immagine richiesta è sempre 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>La densità dei pixel di un dispositivo viene richiesta e servita solo se l'immagine risultante è al di sotto del limite specificato. </p> <p>Il numero di limite si applica alle dimensioni larghezza o altezza. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Se il numero limite è 1600 e la densità dei pixel è 1,5, l’immagine 1500 x 1500 viene servita. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Se il numero limite è 1600 e la densità dei pixel è 2, l’immagine 1000 x 1000 viene trasmessa perché l’immagine 2000 x 2000 supera il limite. </p> </li> 
     </ul> </p> <p><b>Best practice</b>: Il numero limite deve funzionare insieme all’impostazione aziendale per l’immagine con dimensione massima. Pertanto, impostate il numero limite in modo che sia uguale all’impostazione della dimensione massima dell’immagine della società. </p> </td> 
  </tr> 
 </tbody> 
</table>

