---
title: setContainerId
description: Riferimento API di JavaScript per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
TQID: 'https://experienceleague.adobe.com/-JAzFSCKp9cWUljiE-e1362FQGBSR4lfIltdgF0K0Jo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 88
ht-degree: 1%

---

# setContainerId{#setcontainerid}

Riferimento API di JavaScript per il visualizzatore Video360.

` setContainerId( *`containerId`*)`

Imposta l&#39;ID del contenitore DOM (normalmente un DIV) in cui viene inserito il visualizzatore. Non è necessario creare l’elemento contenitore nel momento in cui viene chiamato questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito `init()`. Deve essere chiamato prima di `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l&#39;oggetto JSON `config` al costruttore.

## Parametro {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID contenitore </span> </span> </p> </td> 
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
