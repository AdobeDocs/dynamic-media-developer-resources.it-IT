---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 6%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Imposta su <span class="codeph"> 1</span> per abilitare il precaricamento dell'immagine ingrandita. </p> <p>Impostare su <span class="codeph"> 0</span> per caricare l'immagine di zoom in modo incrementale, in base alle esigenze. </p> <p> <p>Nota:  Tieni presente che se abiliti questa opzione, l’utilizzo della larghezza di banda può risultare notevolmente più elevato, perché l’immagine ingrandita deve essere caricata completamente, anche se l’utente non esegue alcuna azione di zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
