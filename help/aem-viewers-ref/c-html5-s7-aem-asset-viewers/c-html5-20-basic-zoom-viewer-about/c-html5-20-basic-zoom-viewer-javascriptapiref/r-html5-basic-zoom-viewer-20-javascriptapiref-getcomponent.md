---
title: getComponent
description: Riferimento API JavaScript per visualizzatore zoom di base
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: e9bf641f-5bc9-42d9-a030-5591cd883373
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# getComponent{#getcomponent}

Riferimento API JavaScript per visualizzatore zoom di base

`getComponent(componentId)`

Restituisce un riferimento al componente SDK del visualizzatore utilizzato dal visualizzatore. La pagina web può utilizzare questo metodo per estendere o personalizzare il comportamento del visualizzatore predefinito. Chiama questo metodo solo dopo il `initComplete` il callback del visualizzatore è stato eseguito, altrimenti il componente potrebbe non essere ancora stato creato dalla logica del visualizzatore.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` un ID del componente SDK del visualizzatore utilizzato dal visualizzatore. Questo visualizzatore supporta i seguenti ID componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome classe componente SDK per visualizzatore </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> contenitore </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Quando si lavora con le API SDK, è importante utilizzare uno spazio dei nomi SDK corretto e completo, come descritto in Spazio dei nomi SDK per visualizzatore

Per ulteriori informazioni su un particolare componente, consulta la documentazione dell’API SDK per visualizzatori.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Il `{Object}` è un riferimento al componente SDK del visualizzatore. Il metodo restituisce `null` se `componentId` non è un componente visualizzatore supportato o se il componente non è ancora stato creato dalla logica del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```
