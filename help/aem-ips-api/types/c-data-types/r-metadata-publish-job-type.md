---
description: Pubblica i metadati nel server metadati.
solution: Experience Manager
title: MetadataPublishJobType
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: b90d27c0-9398-4597-bcce-3c36a371df22
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 4%

---

# [!DNL MetadataPublishJobType]{#metadatapublishjobtype}

Pubblica i metadati nel server metadati.

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
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3">Impostato su <span class="codeph"> True</span> per pubblicare nuovamente <i>tutti</i> dati nel server metadati. <p>Nota: a seconda della quantità di dati, questa operazione può richiedere da alcuni minuti ad alcune ore. </p><p>Non impostare questo parametro se si desidera pubblicare solo metadati nuovi o modificati. </p></td> 
  </tr> 
 </tbody> 
</table>
