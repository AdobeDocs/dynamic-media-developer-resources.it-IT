---
description: Elimina metadati valori di un risorsa. Funziona con un array di metadati delete per impostare i valori in un batch.
solution: Experience Manager
title: deleteAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ce9b8dff-efc0-4427-9f50-10269647187f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 6%

---

# deleteAssetMetadata{#deleteassetmetadata}

Elimina metadati valori di un risorsa. Utilizza un array di eliminazione dei metadati per impostare i valori in un batch.

Sintassi

## Tipi di utente autorizzati {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Il utente deve aver letto ed eliminato accesso al risorsa.

## Parametri {#section-0eed164e278b456fbdfb7a50727a0416}

**Input (deleteAssetMetadataParam)**

<table id="table_A4438E2FE5F245E5B73F46CD887BE70F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obbligatorio </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>CompanyHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Handle della società a cui appartiene la cartella. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gestione risorsa </p> </td> 
   <td colname="col2"> <p><span class="codeph"> XSD:stringa</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Handle del risorsa da eliminare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>metadatiElimina </p> </td> 
   <td colname="col2"> <p><span class="codeph"> XSD:stringa</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Metadati da eliminare dalla risorsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>deleteArray </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipi:MetadataDeleteArray</span> </p> </td> 
   <td colname="col3"> <p>Sì </p> </td> 
   <td colname="col4"> <p>Array di metadati da eliminare dal risorsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (deleteAssetMetadataParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-d5657289f5234bb0a613dcf691507958}

Eliminazione dei metadati

```java
    <complexType name="MetadataDelete">
        <sequence>
            <element name="fieldHandle" type="xsd:string"/>
        </sequence>
    </complexType>
```

Chiamata di esempio

```java
<ac:Request id="deleteAssetMetadata">
 <deleteAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
  <companyHandle>c|101</companyHandle>
  <assetHandle>a|202</assetHandle>
  <deleteArray>
   <items>
    <fieldHandle>m|2919|ASSET|UntypedUDFField1395788289789</fieldHandle>
   </items>
  </deleteArray>
 </deleteAssetMetadataParam>
</ac:Request>
```
