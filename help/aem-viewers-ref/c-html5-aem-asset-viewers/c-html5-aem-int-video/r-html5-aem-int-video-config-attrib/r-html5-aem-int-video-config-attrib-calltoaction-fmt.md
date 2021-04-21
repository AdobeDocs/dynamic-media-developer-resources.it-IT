---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: CallToAction.fmt
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 38ca592f-329c-4fd4-8dbc-a49000663e55
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# CallToAction.fmt{#calltoaction-fmt}

Attributo di configurazione per Visualizzatore video interattivo.

`[CallToAction.|<containerId>_callToAction.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini. </p> <p>Se il formato specificato termina con "<span class="codeph"> -alpha</span>", il componente esegue il rendering delle immagini come contenuto trasparente. Per tutti gli altri formati di immagine, il componente considera le immagini come opache. </p> </td> 
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
