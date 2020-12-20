---
description: Riferimento API JavaScript per il visualizzatore Video360.
seo-description: Riferimento API JavaScript per il visualizzatore Video360.
seo-title: setLocalizedText
solution: Experience Manager
title: setLocalizedText
topic: Dynamic media
uuid: dd9cf899-8855-463b-a142-698fd1a650fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 2%

---


# setLocalizedText{#setlocalizedtexts}

Riferimento API JavaScript per il visualizzatore Video360.

` setLocalizedTexts( *`localizationInfo`*)`

Imposta i valori SIMBOLO di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima di `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> localizationInfo  </span> </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> Oggetto </span>} JSON con dati di localizzazione. </p> <p>Per ulteriori informazioni, vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localizzazione degli elementi dell'interfaccia utente </a>. </p> <p>Per ulteriori informazioni sul contenuto dell'oggetto, vedere anche la <i>Guida utente dell'SDK per visualizzatori</i>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vedere anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played."},"fr":{"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus."},defaultLocale:"en"})
```

