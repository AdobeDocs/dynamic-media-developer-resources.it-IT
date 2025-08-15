---
title: getComponent
description: JavaScript riferimento API per il visualizzatore Video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a760bc86-b700-4ffe-9983-ef55d88677d6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# getComponent{#getcomponent}

JavaScript riferimento API per il visualizzatore Video interattivo.

`getComponent(componentId)`

Restituisce un riferimento al componente SDK per visualizzatori utilizzato dall&#39;visualizzatore. La pagina Web può utilizzare questo metodo per estendere o personalizzare il comportamento del visualizzatore predefinito. Chiamare questo metodo solo dopo l&#39;esecuzione del `initComplete` callback visualizzatore, altrimenti il componente potrebbe non essere ancora stato creato dalla logica visualizzatore.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` un ID del componente SDK del visualizzatore utilizzato dal visualizzatore. Questo visualizzatore supporta i seguenti ID componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome classe componente SDK per visualizzatori </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Gestione parametri </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> S7SDK. Gestione parametri </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenitore </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Set file multimediali </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lettore video </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoPlayer </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Campioni interattivi </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.InteractiveSwatches </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> callToAction </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.CallToAction </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Volume mutabile </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.MutableVolume </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> playPauseButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PlayPauseButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Cursore di scorrimento video </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoScrubber </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.video.VideoTime </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closedCaptionButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ClosedCaptionButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Controlli </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Condivisione social <span class="codeph"> di </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Condivisione collegamenti </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Quando si utilizzano le API SDK, è importante utilizzare uno spazio dei nomi SDK corretto e completo, come descritto nello [spazio dei nomi SDK](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-html5-viewer-sdk-namespace.md#concept-4ee8657c7d67421f8e7880130a246621) del visualizzatore.

Per ulteriori informazioni su un particolare componente, consulta la documentazione relativa all&#39;API ** di Viewer SDK.

## Rendiconto {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Riferimento al componente SDK per visualizzatori. Il metodo restituisce `null` se il `componentId` componente non è un componente visualizzatore supportato o se il componente non è stato ancora creato dalla logica visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
} 
})
```
