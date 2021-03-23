---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
uuid: 8e989ca7-1ef7-4758-b6b9-c447d7647d1d
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom in linea
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Impostate su <span class="codeph"> 1</span> per abilitare il precaricamento dell'immagine ingrandita, oppure impostate su <span class="codeph"> 0</span> per caricare l'immagine di zoom in modo incrementale, in base alle esigenze. </p> <p> <p>Nota:  Se abiliti questa opzione, l’utilizzo della larghezza di banda può aumentare notevolmente. L’immagine ingrandita viene caricata nella sua interezza, anche se l’utente non avvia un’azione di zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
