---
title: Video360Player.iconeffect
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 7%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Attributo di configurazione per il visualizzatore Video360.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`count`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Abilita la visualizzazione di IconEffect sopra il video quando quest'ultimo è in pausa. Su alcuni dispositivi vengono utilizzati controlli nativi. In tali casi, la <span class="codeph">iconeffect</span> modificatore ignorato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte che IconEffect viene visualizzato e rivisualizzato. Un valore di <span class="codeph"> -1</span> indica che l’icona viene visualizzata di nuovo a tempo indeterminato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dissolvenza</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la durata dell'animazione mostra/nascondi, in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Imposta il numero di secondi in cui IconEffect rimane completamente visibile prima che venga nascosto automaticamente. ovvero il tempo trascorso tra il completamento della dissolvenza in entrata e l'inizio della dissolvenza in uscita. Imposta su <span class="codeph"> 0</span> per disattivare il comportamento Nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
