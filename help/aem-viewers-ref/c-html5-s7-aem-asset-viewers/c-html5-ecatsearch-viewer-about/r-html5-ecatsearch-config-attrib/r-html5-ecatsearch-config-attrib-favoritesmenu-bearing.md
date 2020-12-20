---
description: Specifica la direzione dell'animazione della diapositiva per il contenitore dei pulsanti.
seo-description: Specifica la direzione dell'animazione della diapositiva per il contenitore dei pulsanti.
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic media
uuid: c3f415ad-f976-464a-9067-a5d526908352
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

Specifica la direzione dell&#39;animazione della diapositiva per il contenitore dei pulsanti.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> up|down|left|right|fit-vertical|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Se è impostata su <span class="codeph"> su</span>, <span class="codeph"> giù</span>, <span class="codeph"> sinistra</span> o <span class="codeph"> destra</span>, il pannello si sposta in una direzione specificata senza un ulteriore controllo dei limiti, con conseguente ritaglio del pannello da parte di un contenitore esterno. </p> <p>Quando è impostato su <span class="codeph"> fit-vertical</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore del menu Preferiti e tenta di eseguire il rollout del pannello in una delle seguenti direzioni da tale posizione di base: in basso, a destra, a sinistra. Per ogni tentativo, il componente verifica se il pannello è ritagliato da un contenitore esterno. Se tutti i tentativi non vanno a buon fine, il componente tenta di spostare la posizione del pannello di base verso l’alto e di ripetere i tentativi di implementazione dalla direzione superiore, destra e sinistra. </p> <p>Se impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile. La base viene spostata verso destra, cercando a destra, verso il basso e verso l'alto. Poi sposta la base verso sinistra, provando a sinistra, verso il basso e verso l'alto. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
