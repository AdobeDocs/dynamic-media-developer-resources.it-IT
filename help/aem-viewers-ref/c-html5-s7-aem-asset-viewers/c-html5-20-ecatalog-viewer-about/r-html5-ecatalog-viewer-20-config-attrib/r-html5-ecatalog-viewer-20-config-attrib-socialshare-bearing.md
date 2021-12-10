---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> su|giù|sinistra|destra|fit-verticale|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione diapositiva per il contenitore pulsanti. </p> <p> Quando è impostato su <span class="codeph"> su </span>, <span class="codeph"> giù </span>, <span class="codeph"> sinistra </span>oppure <span class="codeph"> right </span>, il pannello viene eseguito in una direzione specificata senza un controllo aggiuntivo dei limiti. Questo comportamento può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Quando è impostato su <span class="codeph"> adattabile </span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e prova a eseguire il rollout del pannello dal basso, a destra o a sinistra, da tale posizione di base. A ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi non riescono, il componente tenta di spostare la posizione del pannello di base nella parte superiore e ripetere i tentativi di rollout dalla direzione superiore, destra e sinistra. </p> <p>Quando è impostato su <span class="codeph"> adatto </span>, il componente utilizza una logica simile a quella di adattamento verticale. Tuttavia, sposta la base verso destra, verso destra, verso il basso e verso l'alto, e poi sposta la base verso sinistra, cercando le direzioni sinistra, verso il basso e verso l'alto. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8e843b967237426e9a8b3cd0f27b9820}

Facoltativo.

## Predefinito {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Esempio {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
