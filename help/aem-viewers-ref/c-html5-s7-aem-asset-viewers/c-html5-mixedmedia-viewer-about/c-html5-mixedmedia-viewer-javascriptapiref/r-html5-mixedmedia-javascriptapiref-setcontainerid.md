---
description: Riferimento API JavaScript per visualizzatori di file multimediali diversi.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: b6e191dc-3172-45ba-b6f6-258cfbd5855d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Riferimento API JavaScript per visualizzatori di file multimediali diversi.

` setContainerId( *`containerId`*)`

Imposta l’ID del contenitore DOM (in genere un DIV) in cui viene inserito il visualizzatore. Non è necessario che l&#39;elemento contenitore venga creato al momento della chiamata di questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito `init()`. Deve essere chiamato prima di `init()`. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l’oggetto JSON `config` al costruttore.

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
