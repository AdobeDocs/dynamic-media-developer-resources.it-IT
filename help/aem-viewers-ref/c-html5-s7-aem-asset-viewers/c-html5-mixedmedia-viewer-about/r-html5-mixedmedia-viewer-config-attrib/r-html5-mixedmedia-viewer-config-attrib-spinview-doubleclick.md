---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65e2f2c9-ee2c-45a8-9935-a33089b8c379
TQID: 'https://experienceleague.adobe.com/U3RCx6F9hsywdWgtBZukWi6b-Yh5dWzba-2VvxaPMAU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
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
