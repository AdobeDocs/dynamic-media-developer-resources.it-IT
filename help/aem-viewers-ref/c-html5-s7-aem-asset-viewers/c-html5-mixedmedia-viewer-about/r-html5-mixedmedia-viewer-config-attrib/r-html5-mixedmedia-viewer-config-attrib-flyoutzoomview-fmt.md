---
description: Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini.
seo-description: Specifica il formato immagine utilizzato dal componente per caricare le immagini dal server di immagini.
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
uuid: 6f6a69b4-d581-44ff-b089-ce9d0d0170bf
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

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
