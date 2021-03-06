---
title: SocialShare.bearing
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f00b2539-3159-487a-b0fa-9589b694c2e6
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Attributo di configurazione per il visualizzatore Video360.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> su|giù|sinistra|destra|fit-verticale|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione diapositiva per il contenitore pulsanti. </p> <p> Quando è impostato su <span class="codeph"> su</span>, <span class="codeph"> giù</span>, <span class="codeph"> sinistra</span> o <span class="codeph"> destra</span>, il pannello si sporge in una direzione specificata senza un ulteriore controllo dei limiti, il che può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Quando è impostato su <span class="codeph"> fit-verticali</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e cerca di eseguire il rollout del pannello dal basso, a destra o a sinistra da tale posizione di base. A ogni tentativo, il componente controlla se il pannello è troncato da un contenitore esterno. Se tutti i tentativi non riescono, il componente cerca di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di rollout in alto, a destra e a sinistra. </p> <p>Se è impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile. Tuttavia sposta la base a destra prima, provando a destra, giù, e su direzioni di rollout, e poi sposta la base a sinistra, provando a sinistra, giù, e su direzioni di rollout. </p> </td> 
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
