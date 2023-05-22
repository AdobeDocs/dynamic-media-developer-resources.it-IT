---
title: setParams
description: Riferimento API JavaScript per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 32d26999-7815-4c71-ad4c-b7db99ec3d3b
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 2%

---

# setParams{#setparams}

Riferimento API JavaScript per Visualizzatore video interattivo.

` setParams( *`parametri`*)`

Imposta uno o più parametri su un valore specificato. La sintassi dell&#39;argomento del metodo è identica a una stringa di query URL. ovvero rappresenta coppie nome=valore separate da `&`. Come in una stringa di query, i nomi e i valori sono codificati in percentuale utilizzando UTF8. Prima di chiamare `init()`, è necessario chiamare questo parametro.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore sono state trasmesse con `config` Oggetto JSON per il costruttore.

Vedi anche [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).


## Parametro {#section-add05f3d7ca0426897bd74bf7ac9b9cd}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parametri</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> nome=valore coppie di parametri separate da <span class="codeph"> E</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("style=customStyle.css&VideoPlayer.playback=progressive")
```
