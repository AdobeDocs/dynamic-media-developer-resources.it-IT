---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: InteractiveSwatches.fmt
solution: Experience Manager
title: InteractiveSwatches.fmt
topic: Dynamic media
uuid: 0a30c913-39d1-4521-b65c-f2b3879f6928
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Attributo di configurazione per il visualizzatore video interattivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server immagini. </p> <p>Se il formato specificato termina con "<span class="codeph"> -alpha</span>", il componente riproduce le immagini come contenuto trasparente. Per tutti gli altri formati immagine, il componente considera le immagini come opache. Per impostazione predefinita, il componente ha uno sfondo bianco. Per renderlo completamente trasparente, impostate la proprietà CSS <span class="codeph"> background-color</span> su <span class="codeph"> Trasparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`jpeg`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
fmt=png-alpha
```

