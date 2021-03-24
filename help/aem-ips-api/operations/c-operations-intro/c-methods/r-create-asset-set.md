---
description: Crea un set di risorse generico con una stringa di definizione del set non elaborato da pubblicare su un server di immagini.
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 5%

---


# createAssetSet{#createassetset}

Crea un set di risorse generico con una stringa di definizione del set non elaborato da pubblicare su un server di immagini.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> L'handle della società che conterrà il set di risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> L’handle della cartella in cui verrà creato il nuovo set di risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Identificatore univoco creato dal client per il tipo di set di risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Parametri nella stringa di definizione del set. <p>Devono essere risolti nel formato specificato dal visualizzatore di destinazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Gestione della risorsa che funge da miniatura del nuovo set di immagini. Se non viene specificato, IPS cerca di utilizzare la prima risorsa immagine a cui fa riferimento il set. </td> 
  </tr> 
 </tbody> 
</table>

**Funzioni di sostituzione per setDefinition**

È possibile specificare le funzioni di sostituzione in linea risolte durante la ricerca o la pubblicazione del catalogo. Le stringhe di sostituzione hanno il formato `${<substitution_func>}`. Le funzioni disponibili sono enumerate di seguito.

>[!NOTE]
>
>I valori letterali di handle negli elenchi di parametri devono essere racchiusi tra parentesi `([])`. Tutto il testo che si trova al di fuori di una stringa di sostituzione viene copiato verbalmente nella stringa di output durante la risoluzione.

| **Funzione di sostituzione** | **Restituisce** |
|---|---|
| `getFilePath([asset_handle>])` | Percorso del file sorgente principale della risorsa. |
| `getCatalogId([<asset_handle>])` | ID catalogo della risorsa. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valori metadati per la risorsa. |
| `getThumbCatalogId([<asset_handle>])` | L’ID catalogo della risorsa (solo per le risorse basate su immagini). L’ID catalogo della risorsa miniatura associata (per altre risorse). Se una risorsa miniatura associata non è disponibile, la funzione restituisce una stringa vuota. |

**Esempio di stringa setDefinition di file multimediali**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

In fase di ricerca del catalogo o di pubblicazione, questa viene risolta in una stringa simile alla seguente:

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Output (createAssetSet)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sì | L&#39;handle del set di risorse. |

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

