---
title: Condivisione.social
description: Condivisione.social
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
TQID: 'https://experienceleague.adobe.com/sWilQyllf5wtlr-tP1kKtK4L0taRA6HWQW2Yh0MSefQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 1%

---

# Condivisione.social{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> su|giù|sinistra|destra|adatta-verticale|adatta-laterale </span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione di scorrimento per il contenitore pulsanti. </p> <p> Se è impostato su <span class="codeph"> su </span>, <span class="codeph"> su </span>, <span class="codeph"> a sinistra </span> o <span class="codeph"> a destra </span>, il pannello si sposta in una direzione specificata senza un controllo dei limiti aggiuntivi. Questo comportamento può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Se è impostato su <span class="codeph"> adatta a </span> verticale, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e prova a stendere il pannello dalla parte inferiore, destra o sinistra, da tale posizione di base. A ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi hanno esito negativo, il componente tenta di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di rollout dalla direzione superiore, destra e sinistra. </p> <p>Se è impostato su <span class="codeph"> fit-lateral </span>, il componente utilizza una logica simile a quella di fit-vertical. Tuttavia, sposta la base verso destra, prima provando verso destra, verso il basso e verso l'alto verso il basso, quindi sposta la base verso sinistra, provando le direzioni di rollout verso sinistra, verso il basso e verso l'alto. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8e843b967237426e9a8b3cd0f27b9820}

Facoltativo.

## Predefinito {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Esempio {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
