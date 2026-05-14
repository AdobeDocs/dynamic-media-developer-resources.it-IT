---
title: SpinView.singleclick
description: SpinView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 92a497dc-c6b5-4b2d-8095-08bc6ad3d189
TQID: 'https://experienceleague.adobe.com/DkpKrDJuqlcE93u-W3D7F1DwEwxhRet4lP8MHjC-9ZE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# SpinView.singleclick{#spinview-singleclick}

`[SpinView.|<containerId>_spinView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di clic/tocco per eseguire lo zoom. L'impostazione su <span class="codeph"> none </span> disattiva lo zoom con clic/tocco. Se è impostato su <span class="codeph"> rotazione </span> e si fa clic sull'immagine, questa si ingrandisce di un livello; se si fa clic tenendo premuto CTRL l'immagine si riduce di un livello. L'impostazione su <span class="codeph"> reimposta </span> fa sì che un singolo clic sull'immagine ripristini il livello di zoom al livello di rotazione iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`zoomReset` Nei computer desktop; `none` nei dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`singleclick=zoom`
