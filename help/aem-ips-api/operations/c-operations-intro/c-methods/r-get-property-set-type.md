---
description: Ottiene un tipo di set di proprietà utilizzando un handle per una società e il nome del tipo di set di proprietà. Ottiene una struttura di tipo con la maniglia al tipo e al tipo di proprietà.
seo-description: Ottiene un tipo di set di proprietà utilizzando un handle per una società e il nome del tipo di set di proprietà. Ottiene una struttura di tipo con la maniglia al tipo e al tipo di proprietà.
seo-title: getPropertySetType
solution: Experience Manager
title: getPropertySetType
topic: Scene7 Image Production System API
uuid: 203fa949-a81e-455a-a83e-576b6f65e3af
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPropertySetType{#getpropertysettype}

Ottiene un tipo di set di proprietà utilizzando un handle per una società e il nome del tipo di set di proprietà. Ottiene una struttura di tipo con la maniglia al tipo e al tipo di proprietà.

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
| ` *`companyHandle`*` | `xsd:string` | No | L&#39;handle della società. Facoltativo perché un tipo di set di proprietà può appartenere a più società. |
| ` *`name`*` | `xsd:string` | Sì | Nome del tipo di set di proprietà. |

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:PropertySetType</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4">La struttura del tipo che contiene: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Maniglia. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Digitare name. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Tipo di proprietà. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Valore che indica se il tipo consente più tipi di proprietà. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-1b57199415e34a8fa449f864f8895b14}

Questo esempio di codice restituisce un tipo di proprietà impostato per nome.

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

