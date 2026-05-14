---
title: Condivisione.social
description: Attributo di configurazione per il visualizzatore video Ritaglio avanzato.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ef45ba40-661c-4898-a4df-6293ad799a79
TQID: 'https://experienceleague.adobe.com/5b7-Ofn9ZcJTxG-RSwXCbW0pb5EgItA15pG9i2iXUU0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# Condivisione.social{#socialshare-bearing}

Attributo di configurazione per il visualizzatore video Ritaglio avanzato.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> su|giù|sinistra|destra|adatta-verticale|adatta-laterale</span> </p> </td> 
   <td colname="col2"> <p> Specifica la direzione dell'animazione di scorrimento per il contenitore pulsanti. </p> <p> Se è impostato su <span class="codeph"> su</span>, <span class="codeph"> giù</span>, <span class="codeph"> sinistra</span> o <span class="codeph"> destra</span>, il pannello viene eseguito in una direzione specificata senza un controllo dei limiti aggiuntivi, che può causare il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Se è impostato su <span class="codeph"> adatta a verticale</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore di SocialShare e tenta di stendere il pannello dalla parte inferiore, destra o sinistra di tale posizione di base. A ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi hanno esito negativo, il componente tenta di spostare la posizione del pannello di base verso l’alto e ripetere i tentativi di rollout nelle direzioni superiore, destra e sinistra. </p> <p>Se impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile. Tuttavia, sposta la base prima verso destra, provando le direzioni di rollout verso destra, verso il basso e verso l'alto, quindi sposta la base verso sinistra, provando le direzioni di rollout verso sinistra, verso il basso e verso l'alto. </p> </td> 
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
