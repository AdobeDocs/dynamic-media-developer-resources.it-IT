---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_2D828A5750644B9CB95A2989C36F15F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di doppio clic/tocco per eseguire la rotazione. L'impostazione su <span class="codeph"> none </span> disabilita la rotazione tramite doppio clic/tocco. Se è impostato su <span class="codeph">, zoom </span>, facendo clic sull'immagine viene eseguito un passaggio di rotazione; premendo CTRL l'immagine viene eseguito un passaggio di rotazione. L'impostazione su <span class="codeph"> reimposta </span> fa sì che un singolo clic sull'immagine ripristini il livello di rotazione iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di rotazione corrente è pari o superiore al limite specificato, altrimenti viene applicato lo spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`reset` Nei computer desktop; `zoomReset` nei dispositivi touch.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`doubleclick=zoom`
