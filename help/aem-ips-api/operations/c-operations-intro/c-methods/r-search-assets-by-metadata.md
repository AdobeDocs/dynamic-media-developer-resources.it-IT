---
description: Cerca nell'archivio dell'indice dei metadati i termini di ricerca specificati. Restituisce i dati delle risorse come il metodo searchAssets.
solution: Experience Manager
title: searchAssetsByMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 6%

---


# searchAssetsByMetadata{#searchassetsbymetadata}

Cerca nell&#39;archivio dell&#39;indice dei metadati i termini di ricerca specificati. Restituisce i dati delle risorse come il metodo searchAssets.

Mentre `searchAssetsByMetadata` consente di eseguire ricerche nei campi metadati definiti dall&#39;utente, tali campi non vengono restituiti se sono specificati in `responseMetadataArray`. Per illustrare questo punto, nell&#39;esempio di codice seguente:

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

restituisce un valore null:

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

Per risolvere questo problema, puoi utilizzare `fieldHandles` delle risorse restituite dalla ricerca per eseguire `getAssets` (consulta anche [getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca)). Questo metodo ottiene i valori dei campi definiti dall&#39;utente per le risorse in questione. Utilizza il seguente esempio di sintassi per cercare nei campi metadati definiti dall&#39;utente:

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## Tipi di utenti autorizzati {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**Input (searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Il manico per l'azienda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> Filtro</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipo:SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Filtri che consentono di definire i criteri di ricerca. </p> <p>Vedere <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipo:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Condizioni che definiscono i criteri di ricerca. Per ulteriori informazioni, consulta di seguito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:StringArray</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Campi aggiuntivi da compilare nella risposta nel riepilogo risorse. I campi devono essere specificati nel formato normalizzato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Numero di risorse restituite dalla risposta. Il valore predefinito è 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultPage</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Specifica la pagina dei risultati da restituire, in base alle dimensioni della pagina <span class="codeph"> recordsPerPage</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sortBy</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Ordina per campo risorsa selezionato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Scelta del tipo di direzione. Crescente è l'impostazione predefinita. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (searchAssetsByMetadataReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | No | Numero di corrispondenze. |
| `*`assetArray`*` | `types:AssetArray` | No | Array di risorse restituite dalla ricerca. |

## Dettagli metadataConditionArray {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**Struttura dell&#39;articolo**

`metadataConditionArray` la struttura è la seguente:

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**Valori**

`field_handle` è la chiave di ricerca dei metadati. Può contenere la notazione del punto. I valori possibili sono:

* `asset_id` (senza prefisso)
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at` (come  `modified_at` (Data nel modulo: Venerdì 25 luglio 2014 22:13:45 GMT-0500 (CDT))

* `created_by`

**Operatori consentiti**

Il [!DNL operator] definisce come confrontare il valore e includere:

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

Il `comparison_value` è il termine da cercare.

## Esempi {#section-53a12b9c023e4e629eddf5719c955ad4}

Questo esempio di codice esegue una ricerca con i seguenti criteri di metadati:

* `name` il campo contiene  `1000801`.

* `dc.rights` è uguale a  `Per Jessen Schmidt`.

**Request Contents (Richiesta contenuto)**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Risposta**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

