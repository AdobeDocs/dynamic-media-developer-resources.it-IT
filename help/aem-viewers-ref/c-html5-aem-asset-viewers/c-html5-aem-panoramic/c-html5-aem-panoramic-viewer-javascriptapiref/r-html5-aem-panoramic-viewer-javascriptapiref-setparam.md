---
title: setParam
description: Riferimento API JavaScript per il visualizzatore panoramico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 2%

---

# setParam{#setparam}

Riferimento API JavaScript per il visualizzatore panoramico.

` setParam( *`nome, valore`*)`

Imposta il parametro del visualizzatore su un valore specificato. Il parametro è un&#39;opzione di configurazione specifica per il visualizzatore o un modificatore del kit di sviluppo software. Questo parametro viene chiamato prima di `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore sono state passate con `config` Oggetto JSON al costruttore.



<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> nome del parametro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> valore del parametro . Il valore non può essere codificato in percentuale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
