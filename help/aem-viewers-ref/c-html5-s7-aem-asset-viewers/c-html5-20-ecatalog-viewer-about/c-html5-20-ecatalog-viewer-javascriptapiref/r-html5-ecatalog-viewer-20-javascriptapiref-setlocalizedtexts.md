---
description: Riferimento API JavaScript per il visualizzatore video.
solution: Experience Manager
title: setLocalizedText
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 89d6231d-8063-435f-864e-c352287e4764
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

---

# setLocalizedText{#setlocalizedtexts}

Riferimento API JavaScript per il visualizzatore video.

` setLocalizedTexts( *`localizationInfo`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Oggetto</span>} JSON con dati di localizzazione. </p> <p>Per ulteriori informazioni, consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localizzazione degli elementi dell’interfaccia utente</a> . </p> <p>Per ulteriori informazioni sul contenuto dell’oggetto, consulta anche la <i>Guida utente dell’SDK per visualizzatori</i> e l’esempio . </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta i valori SYMBOL di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima di `init()`.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
