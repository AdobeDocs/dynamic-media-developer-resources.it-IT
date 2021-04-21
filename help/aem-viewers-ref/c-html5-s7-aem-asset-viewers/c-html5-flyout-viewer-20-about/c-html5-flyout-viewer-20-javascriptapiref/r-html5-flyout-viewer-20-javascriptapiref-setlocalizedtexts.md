---
description: Riferimento API JavaScript per il visualizzatore a comparsa.
solution: Experience Manager
title: setLocalizedText
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---


# setLocalizedText{#setlocalizedtexts}

Riferimento API JavaScript per il visualizzatore a comparsa.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Oggetto </span>} JSON con dati di localizzazione. </p> <p>Per ulteriori informazioni, consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localizzazione degli elementi dell’interfaccia utente </a> . </p> <p>Per ulteriori informazioni sul contenuto dell’oggetto, consulta la <i>Guida utente dell’SDK per visualizzatori</i> e l’esempio . </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta i valori SYMBOL di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima di `init()`.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom"},"fr":{"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer"},defaultLocale:"en"})
```

