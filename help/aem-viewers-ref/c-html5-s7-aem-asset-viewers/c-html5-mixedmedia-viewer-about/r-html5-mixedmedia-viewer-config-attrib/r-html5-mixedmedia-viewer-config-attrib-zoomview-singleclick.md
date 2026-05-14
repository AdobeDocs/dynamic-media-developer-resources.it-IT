---
title: ZoomView.singleclick
description: ZoomView.singleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0fcc1f5c-a735-430d-be0c-c00ed08830df
TQID: 'https://experienceleague.adobe.com/Bu8BmcQExGK8nex2r9blfXn3p-gV0r8A4t13ILy2c5Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di clic/tocco per eseguire lo zoom. L'impostazione su <span class="codeph"> none </span> disattiva lo zoom con clic/tocco. Se è impostato su <span class="codeph">, lo zoom di </span> facendo clic sull'immagine si ingrandisce di un livello; se si fa clic tenendo premuto CTRL l'immagine si riduce di un livello. L'impostazione su <span class="codeph"> per il ripristino di </span> fa sì che un singolo clic sull'immagine ripristini il livello di zoom iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di zoom corrente è pari o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`zoomReset` nei computer desktop; `none` nei dispositivi touch.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`singleclick=zoom`
