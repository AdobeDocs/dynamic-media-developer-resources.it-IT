---
description: Riferimento API JavaScript per il visualizzatore di eCatalog.
seo-description: Riferimento API JavaScript per il visualizzatore di eCatalog.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 19149e38-b9d2-4ecd-a555-92e2960f7ee3
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

Riferimento API JavaScript per il visualizzatore di eCatalog.

[!DNL ` setContainerId( *`containerId`*)`]

Imposta l’ID del `DOM` contenitore (in genere un `DIV`) in cui viene inserito il visualizzatore. Non è necessario che l&#39;elemento contenitore venga creato nel momento in cui viene chiamato questo metodo. Tuttavia, il contenitore deve esistere quando `init()` viene eseguito. Deve essere chiamato prima `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono trasmesse con l&#39;oggetto `config` JSON al costruttore.

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

