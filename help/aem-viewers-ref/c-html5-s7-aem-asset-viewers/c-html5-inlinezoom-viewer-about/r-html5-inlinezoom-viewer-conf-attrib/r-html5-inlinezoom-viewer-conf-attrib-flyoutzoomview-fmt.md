---
description: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
uuid: 570a9cca-17fa-44d5-b3bb-66ec19453cbc
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom in linea
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 4%

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine che deve essere utilizzato dal componente per caricare le immagini dal server di immagini. Se il formato specificato termina con <span class="codeph"> -alpha</span>, il componente esegue il rendering delle immagini come contenuto trasparente. Per tutti gli altri formati di immagine, il componente considera le immagini come opache. </p> <p>Per impostazione predefinita, il componente dispone di uno sfondo bianco. Pertanto, per renderlo completamente trasparente, imposta la proprietà CSS <span class="codeph"> background-color</span> su <span class="codeph"> trasparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`jpeg`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`fmt=png-alpha`
