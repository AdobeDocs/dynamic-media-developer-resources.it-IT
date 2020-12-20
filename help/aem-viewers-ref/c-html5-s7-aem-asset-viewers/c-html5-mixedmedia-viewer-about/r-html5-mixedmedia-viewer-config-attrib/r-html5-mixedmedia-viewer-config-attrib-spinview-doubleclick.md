---
description: 'null'
seo-description: 'null'
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: 8e78d91e-e4c6-40f1-9421-8da8bc404ee0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di azioni con doppio clic o tocco per le azioni di rotazione. Se si imposta su <span class="codeph"> none </span>, viene disattivato il doppio clic o il tocco. Se impostato su <span class="codeph"> zoom </span> facendo clic sulle rotazioni dell'immagine in un unico passaggio di rotazione, CTRL+clic consente di ruotare un passaggio di rotazione. Se si imposta <span class="codeph"> reset </span>, l'immagine viene reimpostata con un solo clic per ripristinare il livello iniziale di rotazione. Per <span class="codeph"> zoomReset </span>, reimposta se il fattore di rotazione corrente è uguale o superiore al limite specificato, altrimenti viene applicato il spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` su computer desktop;  `zoomReset` su dispositivi touch.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
