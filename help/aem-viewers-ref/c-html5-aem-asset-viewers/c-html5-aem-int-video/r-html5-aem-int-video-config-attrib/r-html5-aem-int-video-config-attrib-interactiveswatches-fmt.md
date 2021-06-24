---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: InteractiveSwatches.fmt
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,Business Practitioner
exl-id: 9a751b91-aeff-4ee1-b2fe-9bec416884ab
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# InteractiveSwatches.fmt{#interactiveswatches-fmt}

Attributo di configurazione per Visualizzatore video interattivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini. </p> <p>Se il formato specificato termina con "<span class="codeph"> -alpha</span>", il componente esegue il rendering delle immagini come contenuto trasparente. Per tutti gli altri formati di immagine, il componente considera le immagini come opache. Per impostazione predefinita, il componente dispone di uno sfondo bianco. Pertanto, per renderlo completamente trasparente, imposta la proprietà CSS <span class="codeph"> background-color</span> su <span class="codeph"> trasparente</span>. </p> </td> 
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
