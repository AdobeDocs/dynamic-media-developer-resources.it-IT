---
title: getComponent
description: Riferimento API JavaScript per visualizzatore zoom in linea
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 72ae83e4-b879-4b3b-a5d9-38ed0fc2969d
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# getComponent{#getcomponent}

Riferimento API JavaScript per visualizzatore zoom in linea

`getComponent(componentId)`

Restituisce un riferimento al componente SDK per visualizzatori utilizzato dal visualizzatore. La pagina web può utilizzare questo metodo per estendere o personalizzare il comportamento del visualizzatore predefinito. Chiama questo metodo solo dopo la `initComplete` il callback del visualizzatore è stato eseguito; in caso contrario, il componente potrebbe non essere ancora creato dalla logica del visualizzatore.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}` un ID del componente SDK per visualizzatori utilizzato dal visualizzatore. Questo visualizzatore supporta i seguenti ID componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome della classe del componente SDK per visualizzatori </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> volo </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.FlyoutZoomView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> campioni </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.Swatches </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Quando lavori con le API SDK, è importante utilizzare correttamente lo spazio dei nomi SDK completo come descritto in [SDK per visualizzatori](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-namespace.md#concept-5af3b472b320496d87735ea612edda80).

Per ulteriori informazioni su un particolare componente, consulta la documentazione SDK per visualizzatori .

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento al componente SDK per visualizzatori. Il metodo restituisce `null` se `componentId` non è un componente visualizzatore supportato o se il componente non è ancora stato creato dalla logica del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyoutZoomView = <instance>.getComponent("flyout"); 
} 
})
```
