---
description: Riferimento API JavaScript per il visualizzatore video.
seo-description: Riferimento API JavaScript per il visualizzatore video.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: c87e9f32-59f9-4f7a-a2cb-89813c00524b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setLocalizedText{#setlocalizedtexts}

Riferimento API JavaScript per il visualizzatore video.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span></span> </p> </td> 
   <td colname="col2"> <p> Oggetto JSON {<span class="codeph"> Object</span>} con dati di localizzazione. </p> <p>Per ulteriori informazioni, consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localizzazione degli elementi</a> dell'interfaccia utente. </p> <p>Per ulteriori informazioni sul contenuto dell’oggetto, consultate anche la Guida <i>utente dell’SDK per</i> visualizzatori e l’esempio. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta i valori SIMBOLO di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima `init()`.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```

