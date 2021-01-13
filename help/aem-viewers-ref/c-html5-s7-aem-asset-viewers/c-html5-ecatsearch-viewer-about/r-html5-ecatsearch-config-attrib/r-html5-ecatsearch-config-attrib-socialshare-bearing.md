---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---


# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral  </span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione della diapositiva per il contenitore dei pulsanti. </p> <p> Quando è impostato su <span class="codeph"> su </span>, <span class="codeph"> giù </span>, <span class="codeph"> sinistra </span> o <span class="codeph"> destra </span>, il pannello si sposta in una direzione specificata senza un controllo aggiuntivo dei limiti. Questo comportamento può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Quando è impostato su <span class="codeph"> fit-vertical </span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e tenta di eseguire il rollout del pannello dal basso, da destra o da sinistra, da tale posizione di base. Per ogni tentativo, il componente verifica se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi non vanno a buon fine, il componente tenta di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di implementazione dalla direzione superiore, destra e sinistra. </p> <p>Se impostato su <span class="codeph"> fit-lateral </span>, il componente utilizza una logica simile a quella con fit-vertical, ma sposta invece la base verso destra, verso il basso e verso l'alto le direzioni di rollout, quindi sposta la base verso sinistra, provando verso sinistra, verso il basso e verso l'alto le direzioni di rollout. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8e843b967237426e9a8b3cd0f27b9820}

Facoltativo.

## Predefinito {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Esempio {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
