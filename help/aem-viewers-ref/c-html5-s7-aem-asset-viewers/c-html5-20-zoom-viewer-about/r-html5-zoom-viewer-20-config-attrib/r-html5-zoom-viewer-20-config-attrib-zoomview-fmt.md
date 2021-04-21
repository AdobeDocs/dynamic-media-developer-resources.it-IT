---
description: ZoomView.fmt
solution: Experience Manager
title: ZoomView.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---


# ZoomView.fmt{#zoomview-fmt}

`[ZoomView.|<containerId>_zoomView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini. Se il formato specificato termina con <span class="codeph"> -alpha</span>, il componente esegue il rendering delle immagini come contenuto trasparente. Per tutti gli altri formati di immagine, il componente considera le immagini come opache. Per impostazione predefinita, il componente dispone di uno sfondo bianco. Pertanto, per renderlo trasparente, imposta la proprietà CSS <span class="codeph"> background-color</span> su <span class="codeph"> trasparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`fmt=png-alpha`
