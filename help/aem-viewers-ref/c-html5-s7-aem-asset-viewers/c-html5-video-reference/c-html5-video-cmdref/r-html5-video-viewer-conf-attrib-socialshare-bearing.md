---
title: SocialShare.bearing
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# SocialShare.bearing{#socialshare-bearing}

Attributo di configurazione per il visualizzatore video.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> su|giù|sinistra|destra|fit-verticale|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione diapositiva per il contenitore pulsanti. </p> <p> Quando è impostato su <span class="codeph"> su</span>, <span class="codeph"> giù</span>, <span class="codeph"> sinistra</span>oppure <span class="codeph"> right</span>, il pannello viene eseguito in una direzione specificata senza un controllo aggiuntivo dei limiti, che può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Quando è impostato su <span class="codeph"> adattabile</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e cerca di eseguire il rollout del pannello dal basso, a destra o a sinistra da tale posizione di base. A ogni tentativo, il componente controlla se il pannello è troncato da un contenitore esterno. Se tutti i tentativi non riescono, il componente cerca di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di rollout in alto, a destra e a sinistra. </p> <p>Quando è impostato su <span class="codeph"> adatto</span>, il componente utilizza una logica simile. Tuttavia sposta la base a destra prima, provando a destra, giù, e su direzioni di rollout, e poi sposta la base a sinistra, provando a sinistra, giù, e su direzioni di rollout. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
