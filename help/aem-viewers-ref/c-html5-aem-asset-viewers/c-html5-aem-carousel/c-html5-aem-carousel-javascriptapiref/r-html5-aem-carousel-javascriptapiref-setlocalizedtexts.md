---
description: Riferimento API JavaScript per il visualizzatore Carosello.
solution: Experience Manager
title: setLocalizedText
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 8ffb8960-187a-43ab-8081-7dfd95d4c75d
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 2%

---

# setLocalizedText{#setlocalizedtexts}

Riferimento API JavaScript per il visualizzatore Carosello.

` setLocalizedTexts( *`localizationInfo`*)`

Imposta i valori SYMBOL di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima di `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Oggetto</span>} JSON con dati di localizzazione. </p> <p>Per ulteriori informazioni, consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> Localizzazione degli elementi dell’interfaccia utente</a> . </p> <p>Per ulteriori informazioni sul contenuto dell’oggetto, consulta anche la <i>Guida utente dell’SDK per visualizzatori</i> e l’esempio . </p> </td> 
  </tr> 
 </tbody> 
</table>

Vedere anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```
