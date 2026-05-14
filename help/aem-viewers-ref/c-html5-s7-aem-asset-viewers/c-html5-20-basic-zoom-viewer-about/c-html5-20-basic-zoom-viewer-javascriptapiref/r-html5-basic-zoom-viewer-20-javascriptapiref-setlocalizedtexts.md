---
title: setLocalizedTexts
description: Riferimento API di JavaScript per visualizzatore zoom di base.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4472ac64-fdab-4f80-985a-29ed8537d235
TQID: 'https://experienceleague.adobe.com/jkYVY45Iv2pRuObA5kh-4Ymvk2Qjeydbgx8ok9yPoc8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 1%

---

# setLocalizedTexts{#setlocalizedtexts}

Riferimento API di JavaScript per visualizzatore zoom di base.

` setLocalizedTexts( *`informazioniLocalizzazione`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> informazioni localizzazione</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Oggetto</span>} oggetto JSON con dati di localizzazione. </p> <p>Per ulteriori informazioni, vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localizzazione degli elementi dell'interfaccia utente</a>. </p> <p> Per ulteriori informazioni sul contenuto dell'oggetto, vedere anche la <i>Guida utente di Viewer SDK</i> e l'esempio. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta i valori del SIMBOLO di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima di `init()`.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"CloseButton.TOOLTIP":"Close"},"fr":{"CloseButton.TOOLTIP":"Fermer"},defaultLocale:"en"})
```
