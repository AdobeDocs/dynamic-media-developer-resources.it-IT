---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura del doppio clic/tocco per attivare le azioni. Se si imposta su <span class="codeph"> none </span>, viene disattivato il doppio clic o il doppio tocco. Se è impostato su <span class="codeph"> zoom </span> facendo clic sull'immagine si verifica un giro in un unico passaggio; CTRL+clic consente di eseguire un passaggio di rotazione. Impostando su <span class="codeph"> reset </span> si reimposta un singolo clic sull'immagine per ripristinare la rotazione al livello iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di rotazione corrente è pari o superiore al limite specificato, altrimenti viene applicato il spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` su computer desktop;  `zoomReset` su dispositivi touch.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
