---
description: ThumbnailGridView.fmt
solution: Experience Manager
title: ThumbnailGridView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# ThumbnailGridView.fmt{#thumbnailgridview-fmt}

`[ThumbnailGridView.|<containerId>_gridView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini. Può essere qualsiasi valore supportato da Image Server e dal browser client. Se il formato specificato termina con <span class="codeph"> -alpha</span>, il componente esegue il rendering delle immagini come contenuto trasparente. Per tutti gli altri formati di immagine, il componente considera le immagini come opache. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-ffe8ccc3a5f2474db47a68c2ad9a96d6}

Facoltativo.

## Predefinito {#section-502c098dbae1452180c7f575a1d9dc8b}

`jpeg`

## Esempio {#section-5cde7b856ba646c293cfd3d79e47c507}

`fmt-png-alpha`
