---
title: setContainerId
description: Riferimento API JavaScript per il visualizzatore a 360 gradi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5859800f-7d01-4c32-a67f-211578d5c50b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Riferimento API JavaScript per il visualizzatore a 360 gradi.

` setContainerId( *`containerId`*)`

Imposta l’ID del contenitore DOM (in genere un DIV) in cui viene inserito il visualizzatore. Non è necessario che l&#39;elemento contenitore venga creato al momento della chiamata di questo metodo. Tuttavia, il contenitore deve esistere quando `init()` viene eseguito. Deve essere chiamato prima `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con `config` Oggetto JSON al costruttore.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID del contenitore. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
