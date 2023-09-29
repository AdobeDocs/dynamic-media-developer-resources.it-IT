---
title: PanoramicView.fmt
description: Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server immagini.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# PanoramicView.fmt{#panoramicview-fmt}

Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server immagini. Se il formato specificato termina con &quot;-alpha&quot;, il componente riproduce le immagini come contenuto trasparente. Per tutti gli altri formati di immagine, il componente tratta le immagini come opache. Per impostazione predefinita, il componente ha uno sfondo trasparente. Pertanto, per renderlo opaco, impostare la `background-color` Proprietà CSS a `desired_color`

`[PanoramicView.|<containerId>_panoramicView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha </span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine da utilizzare per il caricamento delle immagini dal server immagini. Se il formato specificato termina con "-alpha", il componente riproduce le immagini come contenuto trasparente; per tutti gli altri formati, vengono invece trattate come immagini opache. Per impostazione predefinita, il componente ha uno sfondo trasparente. Pertanto, per opacizzare, imposta la proprietà CSS background-color sul colore desiderato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
