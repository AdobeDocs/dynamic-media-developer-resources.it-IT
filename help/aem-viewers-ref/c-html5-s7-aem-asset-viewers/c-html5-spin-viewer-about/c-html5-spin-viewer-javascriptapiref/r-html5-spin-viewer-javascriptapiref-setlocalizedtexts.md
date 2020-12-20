---
description: Riferimento API JavaScript per il visualizzatore 360 gradi.
seo-description: Riferimento API JavaScript per il visualizzatore 360 gradi.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: bf136479-8ac8-4151-8911-377eed631aa2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

---


# setLocalizedText{#setlocalizedtexts}

Riferimento API JavaScript per il visualizzatore 360 gradi.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> Oggetto JSON {<span class="codeph"> Object</span>} con dati di localizzazione. </p> <p>Per ulteriori informazioni, vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Localizzazione di elementi dell'interfaccia utente</a>. </p> <p>Per ulteriori informazioni sul contenuto dell'oggetto, vedere anche la <i>Guida utente dell'SDK per visualizzatori</i>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta i valori SIMBOLO di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima di `init()`.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

