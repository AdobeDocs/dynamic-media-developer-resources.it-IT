---
title: VisualizzazioneZoomAcomparsa.fmt
description: VisualizzazioneZoomAcomparsa.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 6a9a5530-dbde-4090-8545-36bbd7322927
TQID: 'https://experienceleague.adobe.com/F2kNO8NixGhkFPxhfL2DWoUpemxsB-OKqX7X04bsdMU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 3%

---

# VisualizzazioneZoomAcomparsa.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine da utilizzare per il caricamento delle immagini dal server immagini. Se il formato specificato termina con <span class="codeph"> -alpha</span>, il componente riproduce le immagini come contenuto trasparente. Per tutti gli altri formati di immagine, il componente tratta le immagini come opache. </p> <p>Per impostazione predefinita, il componente ha uno sfondo bianco. Per renderlo trasparente, impostare la proprietà CSS <span class="codeph"> background-color</span> su <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
