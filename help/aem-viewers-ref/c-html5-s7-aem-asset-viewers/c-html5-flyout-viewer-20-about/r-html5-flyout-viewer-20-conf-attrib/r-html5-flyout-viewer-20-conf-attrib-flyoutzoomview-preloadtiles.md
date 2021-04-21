---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '70'
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

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
