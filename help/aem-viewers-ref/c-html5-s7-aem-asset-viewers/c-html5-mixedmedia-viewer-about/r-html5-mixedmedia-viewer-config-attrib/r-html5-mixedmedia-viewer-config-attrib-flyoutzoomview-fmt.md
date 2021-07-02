---
description: Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini.
solution: Experience Manager
title: FlyoutZoomView.fmt
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 6e3bf609-eae7-4db9-b922-cba3a9f7634b
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini.

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Se il formato specificato termina con <span class="codeph"> -alpha</span>, il componente esegue il rendering delle immagini come contenuto trasparente. Per tutti gli altri formati immagine, il componente tratta le immagini come opache. </p> <p>Per impostazione predefinita, il componente dispone di uno sfondo bianco. Pertanto, per renderlo completamente trasparente, imposta la proprietà CSS <span class="codeph"> background-color</span> su <span class="codeph"> trasparente</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
