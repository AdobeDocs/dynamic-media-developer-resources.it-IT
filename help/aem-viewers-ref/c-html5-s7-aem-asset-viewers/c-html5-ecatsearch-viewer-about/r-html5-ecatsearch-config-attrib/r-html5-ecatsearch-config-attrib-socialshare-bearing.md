---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> up|down|left|right|fit-vertical|fit-lateral </span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione di scorrimento per il contenitore pulsanti. </p> <p> Se impostato su <span class="codeph"> su </span>, <span class="codeph"> giù </span>, <span class="codeph"> left </span>, o <span class="codeph"> destra </span>, il pannello si sposta in una direzione specificata senza un controllo dei limiti aggiuntivo. Questo comportamento può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Se impostato su <span class="codeph"> fit-vertical </span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e prova a stendere il pannello dalla parte inferiore, destra o sinistra, da tale posizione di base. Ad ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi hanno esito negativo, il componente tenta di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di rollout dalla direzione superiore, destra e sinistra. </p> <p>Se impostato su <span class="codeph"> fit-lateral </span>, il componente utilizza una logica simile a quella con fit-vertical, ma sposta la base a destra prima provando verso destra, verso il basso e verso l'alto le direzioni di rollout, quindi sposta la base a sinistra, provando a sinistra, verso il basso e verso l'alto le direzioni di rollout. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8e843b967237426e9a8b3cd0f27b9820}

Facoltativo.

## Predefinito {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Esempio {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
