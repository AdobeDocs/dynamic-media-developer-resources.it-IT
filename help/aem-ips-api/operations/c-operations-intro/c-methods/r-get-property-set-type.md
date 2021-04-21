---
description: Ottiene un tipo di set di proprietà utilizzando un handle di una società e il nome del tipo di set di proprietà. Ottiene una struttura di tipo con l'handle al tipo e al tipo di proprietà.
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 9%

---


# getPropertySetType{#getpropertysettype}

Ottiene un tipo di set di proprietà utilizzando un handle di una società e il nome del tipo di set di proprietà. Ottiene una struttura di tipo con l&#39;handle al tipo e al tipo di proprietà.

Sintassi

## Tipi di utenti autorizzati {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-c9a53400c44744668bd7915f72d2bf3d}

**Input (getPropertySetTypeParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | No | Il manico per l&#39;azienda. Facoltativo perché un tipo di set di proprietà può appartenere a più società. |
| `*`name`*` | `xsd:string` | Sì | Nome del tipo di set di proprietà. |

**Output (getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PropertySetType</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4">La struttura del tipo che contiene: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Maniglia. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Digitare il nome. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Tipo di proprietà. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Valore che indica se il tipo consente più tipi di proprietà. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-1b57199415e34a8fa449f864f8895b14}

Questo esempio di codice restituisce un set di proprietà per nome.

**Request Contents (Richiesta contenuto)**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**Risposta**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```

