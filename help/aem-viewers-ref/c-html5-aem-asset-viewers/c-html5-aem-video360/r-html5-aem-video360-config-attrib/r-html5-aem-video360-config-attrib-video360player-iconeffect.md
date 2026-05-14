---
title: Video360Player.iconeffect
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 818ea14b-4dab-4447-9645-46f2ba82547b
TQID: 'https://experienceleague.adobe.com/hi-8zIddM3Pybmh38PWiMSYuSY5COz9FnJpZs3FJ6yE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 3%

---

# Video360Player.iconeffect{#video-player-iconeffect}

Attributo di configurazione per il visualizzatore Video360.

` [Video360Player.|<containerId>_video360Player.]iconeffect=0|1[, *`conteggio`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Abilita la visualizzazione di IconEffect sopra il video quando quest'ultimo è in pausa. Su alcuni dispositivi vengono utilizzati controlli nativi. In questi casi, il modificatore <span class="codeph">iconeffect</span> viene ignorato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> conteggio</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte che IconEffect viene visualizzato e rivisualizzato. Il valore <span class="codeph"> -1</span> indica che l'icona viene visualizzata di nuovo indefinitamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dissolvenza <span class="codeph"><span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la durata dell'animazione mostra/nascondi, in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Nascondi automaticamente</span></span> </p> </td> 
   <td colname="col2"> <p> Imposta il numero di secondi in cui IconEffect rimane completamente visibile prima che venga nascosto automaticamente. ovvero il tempo trascorso tra il completamento della dissolvenza in entrata e l'inizio della dissolvenza in uscita. Impostare su <span class="codeph"> 0</span> per disabilitare il comportamento di Nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
