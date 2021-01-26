---
description: Riferimento API JavaScript per il visualizzatore video.
seo-description: Riferimento API JavaScript per il visualizzatore video.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic Media
uuid: a4b741a1-b0b3-4bc3-aeab-9d0e44ec4e79
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

Riferimento API JavaScript per il visualizzatore video.

` setContainerId( *`containerId`*)`

Imposta l&#39;ID del contenitore DOM (in genere un elemento `DIV`) in cui è inserito il visualizzatore. Non è necessario che l&#39;elemento contenitore venga creato nel momento in cui viene chiamato questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito `init()`. Questo parametro viene chiamato prima di `init()`. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono trasmesse con l&#39;oggetto JSON `config` al costruttore.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> ID del contenitore. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

