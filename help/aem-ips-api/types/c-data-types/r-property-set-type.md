---
description: Valori validi per i campi PropertySetType e createPropertySetTypeParam.
solution: Experience Manager
title: PropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0c51e67-6927-4b9f-9935-222e6a194c13
TQID: 'https://experienceleague.adobe.com/yZz7rkrq0rzrrmSH-Wmza-LFExg23GcBp9MKc25wcrE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 4%

---

# [!DNL PropertySetType]{#propertysettype}

Valori validi per i campi PropertySetType e createPropertySetTypeParam.

I valori includono:

* `UserProperty`
* `CompanyProperty`
* `UserCompanyProperty`

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Digita l’handle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Gestore azienda. <p>Nota: il tipo è globale se l'handle della società non è presente. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Digita il nome. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Uno dei tipi di set di proprietà. Vedere Input (<span class="codeph"> createPropertySetTypeParam</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> allowMultiple</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Specifica se consentire l'associazione di più istanze del set di proprietà a un oggetto per questo tipo. </td> 
  </tr> 
 </tbody> 
</table>
