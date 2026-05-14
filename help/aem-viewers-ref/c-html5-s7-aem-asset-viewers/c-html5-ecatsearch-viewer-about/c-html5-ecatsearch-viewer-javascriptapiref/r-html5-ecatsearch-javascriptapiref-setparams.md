---
description: Riferimento API di JavaScript per il visualizzatore eCatalog.
solution: Experience Manager
title: setParams
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cbd7987b-5e47-4ac0-8235-a217e5e6dee9
TQID: 'https://experienceleague.adobe.com/NOaYrj9ntatmLob6D2xY-MxJEGBMGkZYHoo04HXMeOY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 1%

---

# setParams{#setparams}

Riferimento API di JavaScript per il visualizzatore eCatalog.

[!DNL ` setParams( *`parametri`*)`]

Imposta uno o più parametri su un valore specificato. La sintassi dell&#39;argomento del metodo è identica a una stringa di query URL. Rappresenta cioè coppie nome=valore separate da [!DNL `&`]. Proprio come in una stringa di query, i nomi e i valori sono codificati in percentuale utilizzando UTF8. Prima di chiamare [!DNL `init()`], è necessario chiamare questo parametro.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l&#39;oggetto JSON [!DNL `config`] al costruttore.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> parametri</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}</span> coppie nome=valore separate da <span class="codeph"> &amp;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParams("PageView.zoomstep=2,3&PageView.iscommand=op_sharpen%3d1")
```
