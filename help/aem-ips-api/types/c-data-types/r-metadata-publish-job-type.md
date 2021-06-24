---
description: Pubblica i metadati sul server di metadati.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic, SDK/API, Metadati
role: Developer,Administrator
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 5%

---

# MetadataPublishJobType{#metadatapublishjobtype}

Pubblica i metadati sul server di metadati.

Sintassi

## Parametri {#section-6c51fa689b3648fbb7c7945a7e176d0a}

<table id="table_23B5CFC5C3F946F9AFDB6A83A1AAB7AF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> forcePublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3">Impostare su <span class="codeph"> True</span> per pubblicare di nuovo i dati <i>all</i> nel server di metadati. <p>Nota:  A seconda della quantità di dati, questo può richiedere alcuni minuti a poche ore. </p><p>Non impostare questo parametro se desideri pubblicare solo metadati nuovi o modificati. </p></td> 
  </tr> 
 </tbody> 
</table>
