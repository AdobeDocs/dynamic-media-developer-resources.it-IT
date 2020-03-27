---
description: 'null'
seo-description: 'null'
seo-title: PageView.fmt
solution: Experience Manager
title: PageView.fmt
topic: Dynamic media
uuid: 302e20bf-d398-45de-98a5-58b9edde48f3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PageView.fmt{#pageview-fmt}

`[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server immagini. Se il formato specificato termina con <span class="codeph"> -alpha</span>, il componente riproduce le immagini come contenuto trasparente. Per tutti gli altri formati immagine, il componente considera le immagini come opache. Per impostazione predefinita, il componente ha uno sfondo bianco. Per renderlo trasparente, impostate la proprietà CSS <span class="codeph"> background-color</span> su <span class="codeph"> Trasparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Facoltativo.

## Predefinito {#section-4b6a350501124ffa9a6b1b71b32eff5d}

`jpeg`

## Esempio {#section-7de29e43bb3640e4aa1f8984b4afddad}

`fmt=png-alpha`
