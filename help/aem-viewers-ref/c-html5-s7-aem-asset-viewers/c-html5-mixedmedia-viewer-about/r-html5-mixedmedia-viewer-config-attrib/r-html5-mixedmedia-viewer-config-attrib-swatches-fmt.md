---
description: Swatches.fmt
solution: Experience Manager
title: Swatches.fmt
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,User
exl-id: 043196c8-63ab-439e-a28f-b76d1467f26e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# Swatches.fmt{#swatches-fmt}

`[Swatches.|<containerId>_swatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_4620F51BD77149FDB68F1FBECC443801"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td> <p>Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini. Se il formato specificato termina con <span class="codeph"> -alpha</span>, il componente esegue il rendering delle immagini come contenuto trasparente. Per tutti gli altri formati di immagine, il componente considera le immagini come opache. Per impostazione predefinita, il componente dispone di uno sfondo bianco. Pertanto, per rendere lo sfondo trasparente, imposta la proprietà CSS <span class="codeph"> background-color</span> su <span class="codeph"> trasparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt-png-alpha`
