---
description: Crea o modifica un campo di metadati. Ometti la maniglia del campo opzionale per creare un nuovo campo di metadati.
solution: Experience Manager
title: saveMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 8%

---


# saveMetadataField{#savemetadatafield}

Crea o modifica un campo di metadati. Ometti la maniglia del campo opzionale per creare un nuovo campo di metadati.

>[!NOTE]
>
>Questo metodo è obsoleto.

## Tipi di utenti autorizzati {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-ec6827d485a143f4a059a92b18e40f4e}

**Input (saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome parametro </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obbligatorio </th> 
   <th colname="col4" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Il manico per l'azienda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Maniglia del campo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Scelta dei tipi di risorse da cui salvare i metadati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome campo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Scelta dei tipi di campi di metadati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Valore predefinito dei campi per tutte le risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Nascondere o esporre metadati specifici del sistema IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforcement</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Flag booleano che indica se il campo metadati è applicato (convalidato) quando il valore è impostato. </p> <p>Se è impostato su true, viene generato un errore se un valore non valido è impostato in <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (saveMetadataFieldReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | Sì | Gestione del nuovo campo metadati. |

## Esempi {#section-4441c26d1f41466ba972b43dd5189e89}

Questo esempio di codice crea un nuovo campo metadati vincolato dalle costanti di stringa Tipo di risorsa e Tipi di campi metadati . Se l&#39;elemento `fieldHandle` ha un valore di handle di campo valido, modifica i valori dei metadati e ottiene lo stesso handle di campo specificato nella richiesta.

**Request Contents (Richiesta contenuto)**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**Risposta**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```

