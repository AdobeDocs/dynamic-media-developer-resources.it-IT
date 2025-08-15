---
title: SmartCropVideoPlayer.iconeffect
description: Attributo di configurazione per il visualizzatore video Ritaglio avanzato.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 369e389c-f0e2-405e-b4aa-2f6b9ac8b8ea
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# SmartCropVideoPlayer.iconeffect{#smartcropvideoplayer-iconeffect}

Attributo di configurazione per il visualizzatore video Ritaglio avanzato.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *`conteggio`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Abilita la visualizzazione di IconEffect sopra il video quando questo viene messo in pausa. Su alcuni dispositivi vengono utilizzati controlli nativi. In tal caso, il modificatore iconeffect<span class="codeph"> di </span> viene ignorato. </p> </td> 
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
