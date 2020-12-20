---
description: Attributo di configurazione per il visualizzatore Video360.
seo-description: Attributo di configurazione per il visualizzatore Video360.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

Attributo di configurazione per il visualizzatore Video360.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione della diapositiva per il contenitore dei pulsanti. </p> <p> Se impostato su <span class="codeph"> su</span>, <span class="codeph"> giù</span>, <span class="codeph"> sinistra</span> o <span class="codeph"> destra</span>, il pannello si sposta in una direzione specificata senza un controllo aggiuntivo dei limiti, il che può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Quando è impostato su <span class="codeph"> fit-vertical</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e tenta di eseguire il rollout del pannello dal basso, a destra o a sinistra da tale posizione di base. Per ogni tentativo, il componente verifica se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi non vanno a buon fine, il componente tenta di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di implementazione nella direzione superiore, destra e sinistra. </p> <p>Se impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile. Tuttavia, sposta la base verso destra, cercando a destra, verso il basso e verso l'alto le direzioni di rollout, e poi sposta la base verso sinistra, provando a sinistra, verso il basso e verso l'alto le direzioni di rollout. </p> </td> 
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

