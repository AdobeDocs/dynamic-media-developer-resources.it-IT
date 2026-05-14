---
title: MenuPreferiti.cuscinetto
description: Specifica la direzione dell'animazione di scorrimento per il contenitore pulsanti.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
TQID: 'https://experienceleague.adobe.com/zWVKT6TznkJpBNJ74-vkCnfNkgjBiGJ0dKRVsQnEwvs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 1%

---

# MenuPreferiti.cuscinetto{#favoritesmenu-bearing}

Specifica la direzione dell&#39;animazione di scorrimento per il contenitore pulsanti.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> su|giù|sinistra|destra|adatta-verticale|adatta-laterale</span> </p> </td> 
   <td colname="col2"> <p> Se è impostato su <span class="codeph"> su</span>, <span class="codeph"> giù</span>, <span class="codeph"> sinistra</span> o <span class="codeph"> destra</span>, il pannello si sposta nella direzione specificata senza un controllo dei limiti aggiuntivi, causando il ritaglio del pannello da parte di un contenitore esterno. </p> <p>Se è impostato su <span class="codeph"> adatta a verticale</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore del menu Preferiti. Tenta di stendere il pannello in una delle seguenti direzioni da tale posizione di base: basso, destra, sinistra. A ogni tentativo, il componente controlla se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi hanno esito negativo, il componente tenta di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di rollout da una direzione superiore, destra e sinistra. </p> <p>Se impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile. La base viene spostata dapprima verso destra, quindi verso destra, verso il basso e verso l'alto. Quindi, sposta la base verso sinistra, provando le direzioni di scorrimento verso sinistra, verso il basso e verso l'alto. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
