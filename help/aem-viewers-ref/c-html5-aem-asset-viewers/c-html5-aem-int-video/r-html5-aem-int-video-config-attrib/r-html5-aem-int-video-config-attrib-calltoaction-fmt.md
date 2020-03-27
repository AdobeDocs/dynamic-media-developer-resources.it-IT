---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: CallToAction.fmt
solution: Experience Manager
title: CallToAction.fmt
topic: Dynamic media
uuid: c85160e2-431f-42af-a468-c754bfe86ecd
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.fmt{#calltoaction-fmt}

Attributo di configurazione per il visualizzatore video interattivo.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server immagini. </p> <p>Se il formato specificato termina con "<span class="codeph"> -alpha</span>", il componente riproduce le immagini come contenuto trasparente. Per tutti gli altri formati immagine, il componente considera le immagini come opache. </p> </td> 
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

