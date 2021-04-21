---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> su|giù|sinistra|destra|fit-verticale|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione diapositiva per il contenitore pulsanti. </p> <p> Quando è impostato su <span class="codeph"> su </span>, <span class="codeph"> giù </span>, <span class="codeph"> a sinistra </span> o <span class="codeph"> a destra </span>, il pannello si sporge in una direzione specificata senza un ulteriore controllo dei limiti. Questo comportamento può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Quando è impostato su <span class="codeph"> fit-verticali </span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e cerca di eseguire il rollout del pannello dal basso, a destra o a sinistra, da tale posizione di base. A ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi non riescono, il componente cerca di spostare la posizione del pannello di base nella parte superiore e di ripetere i tentativi di rollout dalla direzione superiore, destra e sinistra. </p> <p>Quando è impostato su <span class="codeph"> fit-lateral </span>, il componente utilizza una logica simile a quella di fit-verticali, ma sposta invece la base verso destra, verso il basso e verso l'alto le direzioni di rollout, quindi sposta la base verso sinistra, provando verso sinistra, verso il basso e verso l'alto le direzioni di rollout. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8e843b967237426e9a8b3cd0f27b9820}

Facoltativo.

## Predefinito {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Esempio {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
