---
description: Riferimento API JavaScript per il visualizzatore di immagini video.
seo-description: Riferimento API JavaScript per il visualizzatore di immagini video.
seo-title: getComponent
solution: Experience Manager
title: getComponent
topic: Dynamic Media
uuid: 6dd112f1-7b34-4d04-969e-b0cef46b4ad4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 1%

---


# getComponent{#getcomponent}

Riferimento API JavaScript per il visualizzatore di immagini video.

`getComponent(componentId)`

Restituisce un riferimento al componente SDK per visualizzatori usato dal visualizzatore. La pagina Web può usare questo metodo per estendere o personalizzare il comportamento del visualizzatore predefinito. Richiamate questo metodo solo dopo l&#39;esecuzione del callback del visualizzatore `initComplete`. In caso contrario, il componente potrebbe non essere ancora creato dalla logica del visualizzatore.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` -  `{String}` un ID del componente SDK per visualizzatori usato dal visualizzatore. Questo visualizzatore supporta i seguenti ID componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome classe componente SDK per visualizzatori </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> container  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mediaSet  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomView  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ZoomView  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.mageMapEffect  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Quando lavori con le API SDK, è importante utilizzare lo spazio dei nomi SDK completo corretto come descritto in [Spazio dei nomi SDK del visualizzatore](../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-namespace.md#concept-00a31b9bc7eb4014b28c1ba661fe5265).

Per ulteriori informazioni su un particolare componente, consultate la documentazione API SDK per visualizzatori.

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` un riferimento al componente SDK per visualizzatori. Il metodo restituisce `null` se il `componentId` non è un componente visualizzatore supportato o se il componente non è ancora stato creato dalla logica del visualizzatore.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
} 
})
```

