---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---

# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> adatto laterale|adatta verticale</span> </p> </td> 
   <td> <p> Controlla la direzione dell’aspetto del pannello a discesa. </p> <p>Quando è impostato su <span class="codeph"> fit-Vertical</span>, il componente sposta prima la posizione del pannello di base nella parte inferiore del relativo pulsante e cerca di eseguire il rollout del pannello a destra o a sinistra dalla posizione di base. A ogni tentativo, il componente controlla se il pannello è troncato da un contenitore esterno. Se tutti i tentativi non riescono, il componente tenta di spostare la posizione del pannello di base verso l’alto e ripetere i tentativi di rollout nella direzione destra e sinistra. </p> <p>Quando è impostato su <span class="codeph"> fit-lateral</span>, il componente utilizza una logica simile, ma sposta la base a destra prima, provando a scorrere verso il basso e verso l'alto le direzioni di rollout. Poi sposta la base a sinistra, provando giù e su le direzioni di rotolamento. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Imposta il ritardo in secondi del timer di mascheramento automatico del menu a discesa che nasconde il pannello quando un utente è inattivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-55436ddd78b04f538dbb9a7a8463feae}

Facoltativo.

## Predefinito {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Esempio {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
