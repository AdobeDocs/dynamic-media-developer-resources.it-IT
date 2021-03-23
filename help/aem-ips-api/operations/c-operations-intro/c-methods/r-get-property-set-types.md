---
description: Ottiene i tipi di set di proprietà associati alla società specificata o i tipi di set di proprietà globali se non viene specificata alcuna società.
seo-description: Ottiene i tipi di set di proprietà associati alla società specificata o i tipi di set di proprietà globali se non viene specificata alcuna società.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 9%

---


# getPropertySetTypes{#getpropertysettypes}

Ottiene i tipi di set di proprietà associati alla società specificata o i tipi di set di proprietà globali se non viene specificata alcuna società.

Sintassi

## Tipi di utenti autorizzati {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-ac3ed9e036b54ea993f544046ff0e15d}

**Input (getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obbligatorio </th> 
   <th colname="col4" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">L'handle della società a cui sono associati i tipi di set di proprietà. <p>Ometti se desideri restituire i tipi di set di proprietà globali. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getPropertySetTypesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | Sì | Matrice di tipi di set di proprietà associati alla società specificata o di tipi di set di proprietà globali, se non è stata specificata alcuna società. |

## Esempi {#section-280c406a90864409856aee44d4069a52}

**Request Contents (Richiesta contenuto)**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**Risposta**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

