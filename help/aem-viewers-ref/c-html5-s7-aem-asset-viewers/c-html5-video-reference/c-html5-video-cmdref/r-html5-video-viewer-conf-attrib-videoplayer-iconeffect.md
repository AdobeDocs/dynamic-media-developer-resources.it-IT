---
title: VideoPlayer.iconeffect
description: Attributo di configurazione per Visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: b283b495-ee28-4f9d-ad4d-b14ac2f9a1a2
TQID: 'https://experienceleague.adobe.com/rRsq1iu6-XNI-4orEgNaZ7hCzVx22v2X7hLbQvliQs4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 4%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Attributo di configurazione per Visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`conteggio`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Abilita la visualizzazione di IconEffect sopra il video quando questo viene messo in pausa. Su alcuni dispositivi vengono utilizzati controlli nativi. In tal caso, il modificatore iconeffect</span> di <span class="codeph"> viene ignorato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> conteggio</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte che IconEffect viene visualizzato e rivisualizzato. Il valore <span class="codeph"> -1</span> indica che l'icona viene visualizzata di nuovo indefinitamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Dissolvenza <span class="codeph"> <span class="varname"></span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica la durata dell'animazione mostra/nascondi, in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Imposta il numero di secondi in cui IconEffect rimane visibile prima che venga nascosto automaticamente. ovvero il tempo trascorso tra il completamento dell'animazione di dissolvenza in entrata e l'inizio dell'animazione di dissolvenza in uscita. L'impostazione <span class="codeph"> 0</span> disattiva il comportamento di Nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```
