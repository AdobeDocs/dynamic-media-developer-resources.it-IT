---
description: Specifica la direzione dell'animazione diapositiva per il contenitore pulsanti.
solution: Experience Manager
title: FavoritesMenu.bearing
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,Business Practitioner
exl-id: 2466a288-59c2-4a5e-b0bd-ff5b42dcacdb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Specifica la direzione dell&#39;animazione diapositiva per il contenitore pulsanti.

[!DNL `[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> su|giù|sinistra|destra|fit-verticale|fit-lateral</span> </p> </td> 
   <td colname="col2"> <p> Quando è impostato su <span class="codeph"> su</span>, <span class="codeph"> giù</span>, <span class="codeph"> sinistra</span> o <span class="codeph"> destra</span>, il pannello si sporge nella direzione specificata senza un ulteriore controllo dei limiti, il che si traduce nel ritaglio del pannello da parte di un contenitore esterno. </p> <p>Quando è impostato su <span class="codeph"> fit-verticali</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore del menu Preferiti e cerca di eseguire il rollout del pannello in una delle seguenti direzioni da tale posizione di base: in basso, a destra, a sinistra. A ogni tentativo, il componente controlla se il pannello è troncato da un contenitore esterno. Se tutti i tentativi non riescono, il componente tenta di spostare la posizione del pannello di base nella parte superiore e ripetere i tentativi di rollout da una direzione superiore, destra e sinistra. </p> <p>Se è impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile. La base viene spostata a destra prima, provando a destra, giù, e su direzione di rotolamento. Poi sposta la base a sinistra, provando a sinistra, giù e su direzione di rotolamento. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fit-vertical`]

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `bearing=left`]
