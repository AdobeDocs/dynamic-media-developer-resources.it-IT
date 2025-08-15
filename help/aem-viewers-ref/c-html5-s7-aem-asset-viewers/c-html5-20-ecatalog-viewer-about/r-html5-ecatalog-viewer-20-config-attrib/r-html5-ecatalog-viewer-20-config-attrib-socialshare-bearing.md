---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> su|giù|sinistra|destra|adatta-verticale|adatta-laterale </span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell diapositiva animazione per il contenitore dei pulsanti. </p> <p> Se impostato su <span class="codeph"> su </span>, <span class="codeph"> giù </span>, <span class="codeph"> sinistra </span>o <span class="codeph"> destra </span>, il pannello si srotola in una direzione specificata senza ulteriori controlli dei limiti. Questo comportamento può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Se impostato su <span class="codeph"> fit-vertical, </span>il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e prova a stendere il pannello dal basso, a destra o a sinistra, da tale posizione di base. Ad ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi falliscono, il componente tenta di spostare la posizione del pannello di base verso l'alto e ripetere i rollout tentativi dalla direzione superiore, destra e sinistra. </p> <p>Se impostato su <span class="codeph"> fit-lateral </span>, il componente utilizza una logica simile a quella di fit-vertical. Tuttavia, sposta la base verso destra prima - provando le direzioni di srotolamento a destra, in basso e in alto - quindi sposta la base a sinistra, provando le direzioni di sinistra, giù e su rollout. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8e843b967237426e9a8b3cd0f27b9820}

Facoltativo.

## Predefinito {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Esempio {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
