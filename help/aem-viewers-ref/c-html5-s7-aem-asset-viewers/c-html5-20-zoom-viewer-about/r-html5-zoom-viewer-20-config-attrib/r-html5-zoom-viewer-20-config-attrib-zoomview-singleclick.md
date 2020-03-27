---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.singleclick
solution: Experience Manager
title: ZoomView.singleclick
topic: Dynamic media
uuid: 919dd48e-b621-4dbb-9cae-f2d0f91f45a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.singleclick{#zoomview-singleclick}

`[ZoomView.|<containerId>_zoomView.]singleclick=none|zoom|reset|zoomReset`

<table id="table_82C9252157DB41B5B98505855975D2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di zoom con un solo clic o tocco. Se si imposta su <span class="codeph"> none, </span> lo zoom con un solo clic o un tocco viene disattivato. Se è impostato per <span class="codeph"> lo zoom, facendo </span> clic sull’immagine si esegue lo zoom in un passaggio di zoom; CTRL+clic consente di ridurre un passaggio di zoom. Se si imposta la <span class="codeph"> reimpostazione, </span> si fa clic sull’immagine per ripristinare lo zoom al livello iniziale. Per <span class="codeph"> lo zoomReset </span>, viene applicato il reset se il fattore di zoom corrente è uguale o superiore al limite specificato, altrimenti viene applicato lo zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`zoomReset` su computer desktop; `none` su dispositivi touch.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`singleclick=zoom`
