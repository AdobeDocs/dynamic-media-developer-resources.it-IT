---
title: setLocalizedTexts
description: Riferimento API di JavaScript per il visualizzatore di file multimediali diversi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 19bc61be-4321-434a-ae2c-4576c7799c0a
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 1%

---

# setLocalizedTexts{#setlocalizedtexts}

Riferimento API di JavaScript per il visualizzatore di file multimediali diversi.

` setLocalizedTexts( *`informazioniLocalizzazione`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> informazioni localizzazione</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Oggetto</span>} oggetto JSON con dati di localizzazione. </p> <p>Per ulteriori informazioni, vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localizzazione degli elementi dell'interfaccia utente</a>. </p> <p>Per ulteriori informazioni sul contenuto dell'oggetto, vedere anche la <i>Guida utente di Viewer SDK</i> e l'esempio. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta i valori del SIMBOLO di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima di `init()`.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
