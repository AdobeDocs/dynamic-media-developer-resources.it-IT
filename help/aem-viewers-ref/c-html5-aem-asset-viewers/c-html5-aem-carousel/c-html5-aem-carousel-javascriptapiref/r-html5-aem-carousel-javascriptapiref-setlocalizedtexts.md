---
title: setLocalizedTexts
description: Riferimento API di JavaScript per il visualizzatore carosello.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8ffb8960-187a-43ab-8081-7dfd95d4c75d
TQID: 'https://experienceleague.adobe.com/TTXDIex6bBbzCZj5A4hnlNUmN5Id2tjphlGbBsXslJw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 69
ht-degree: 1%

---

# setLocalizedTexts{#setlocalizedtexts}

Riferimento API di JavaScript per il visualizzatore carosello.

` setLocalizedTexts( *`informazioniLocalizzazione`*)`

Imposta i valori del SIMBOLO di localizzazione per una o più impostazioni internazionali. Questo parametro deve essere chiamato prima di `init()`.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> informazioni localizzazione</span> </span> </p> </td> 
   <td colname="col2"> <p> {<span class="codeph"> Oggetto</span>} oggetto JSON con dati di localizzazione. </p> <p>Per ulteriori informazioni, vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md" format="dita" scope="local"> Localizzazione degli elementi dell'interfaccia utente</a>. </p> <p>Per ulteriori informazioni sul contenuto dell'oggetto, vedere anche la <i>Guida utente di Viewer SDK</i> e l'esempio. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vedi anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setLocalizedTexts({"en":{"PanLeftButton.TOOLTIP":"Left"},"fr":{"PanLeftButton.TOOLTIP":"Gauchiste"},defaultLocale:"en"})
```
