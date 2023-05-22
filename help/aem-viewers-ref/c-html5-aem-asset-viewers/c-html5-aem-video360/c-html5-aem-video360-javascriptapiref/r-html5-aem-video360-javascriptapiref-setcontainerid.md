---
title: setContainerId
description: Riferimento API JavaScript per Visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Riferimento API JavaScript per Visualizzatore Video360.

` setContainerId( *`containerId`*)`

Imposta l&#39;ID del contenitore DOM (normalmente un DIV) in cui viene inserito il visualizzatore. Non è necessario creare l’elemento contenitore nel momento in cui viene chiamato questo metodo. Tuttavia, il contenitore deve esistere quando `init()` viene eseguito. Deve essere chiamato prima di `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono trasmesse con `config` Oggetto JSON al costruttore.

## Parametro {#section-fa807db629ce43bab286b1e1dc96c492}

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
