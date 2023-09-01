---
title: createAssetSet
description: Crea un set di risorse generico con una stringa di definizione del set non elaborato da pubblicare su un server immagini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 5%

---

# createAssetSet{#createassetset}

Crea un set di risorse generico con una stringa di definizione del set non elaborato da pubblicare su un server immagini.

Sintassi

## Tipi di utenti autorizzati {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-3580b586296e42a5b21426085b1bb72d}

**Input (createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Handle dell’azienda contenente il set di risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Handle della cartella in cui viene creato il nuovo set di risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Identificatore univoco creato dal client per il tipo di set di risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Parametri nella stringa di definizione del set. <p>Questi parametri devono essere risolti nel formato specificato dal visualizzatore di destinazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Handle della risorsa che funge da miniatura per il nuovo set di immagini. Se non viene specificato diversamente, IPS tenta di utilizzare la prima risorsa immagine a cui fa riferimento il set. </td> 
  </tr> 
 </tbody> 
</table>

**Funzioni di sostituzione per setDefinition**

È possibile specificare funzioni di sostituzione in linea risolte durante la ricerca o la pubblicazione del catalogo. Le stringhe di sostituzione hanno il formato `${<substitution_func>}`. Le funzioni disponibili sono descritte di seguito.

>[!NOTE]
>
>I valori letterali degli handle negli elenchi dei parametri devono essere racchiusi tra parentesi quadre `([])`. Tutto il testo che si trova all&#39;esterno di una stringa di sostituzione viene copiato letteralmente nella stringa di output durante la risoluzione.

| **Funzione di sostituzione** | **Restituisce** |
|---|---|
| `getFilePath([asset_handle>])` | Percorso del file di origine principale della risorsa. |
| `getCatalogId([<asset_handle>])` | ID catalogo della risorsa. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valori dei metadati della risorsa. |
| `getThumbCatalogId([<asset_handle>])` | ID catalogo della risorsa (solo per risorse basate su immagini). ID catalogo della risorsa miniatura associata (per altre risorse). Se una risorsa miniatura associata non è disponibile, la funzione restituisce una stringa vuota. |

**Stringa Media SetDefinition di esempio**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Al momento della ricerca del catalogo o della pubblicazione, questo processo viene risolto in una stringa simile alla seguente:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Output (createAssetSet)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| assetHandle | `xsd:string` | Sì | Handle del set di risorse. |

## Esempi {#section-fed53089de824d67ab96cd9103d384b4}

**Request Contents (Richiesta contenuto)**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**Risposta**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```
