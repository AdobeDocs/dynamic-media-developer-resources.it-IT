---
description: Riferimento API JavaScript per il visualizzatore Video360.
seo-description: Riferimento API JavaScript per il visualizzatore Video360.
seo-title: setParams
solution: Experience Manager
title: setParams
topic: Dynamic Media
uuid: 0a5b9798-0e3f-4310-9b6e-0214a420951b
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---


# setParams{#setparams}

Riferimento API JavaScript per il visualizzatore Video360.

` setParams( *`params`*)`

Imposta uno o più parametri su un valore specificato. La sintassi dell&#39;argomento metodo è identica a una stringa di query URL. Rappresenta cioè coppie nome=valore separate da `&`. Come in una stringa di query, i nomi e i valori sono codificati in percentuale con UTF8. Prima di chiamare `init()`, questo parametro deve essere chiamato.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore sono state passate con l&#39;oggetto JSON `config` al costruttore.

Vedere anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Parametro {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> params</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> name=valore, coppie di parametri separate da  <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```

