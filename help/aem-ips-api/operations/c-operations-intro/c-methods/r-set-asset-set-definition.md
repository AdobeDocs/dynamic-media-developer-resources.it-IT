---
description: Aggiorna la definizione del set per un set di risorse esistente.
seo-description: Aggiorna la definizione del set per un set di risorse esistente.
seo-title: setAssetSetDefinition
solution: Experience Manager
title: setAssetSetDefinition
topic: Dynamic Media Image Production System API
uuid: 2a2dce5d-7a01-49af-ac8b-33ae0b234ecc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 5%

---


# setAssetSetDefinition{#setassetsetdefinition}

Aggiorna la definizione del set per un set di risorse esistente.

Sintassi

## Tipi di utenti autorizzati {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Input (setAssetDefinitionParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle della società con il set di risorse. |
| `*`assetHandle`*` | `xsd:string` | Sì | handle set di risorse |
| `*`setDefinition`*` | `xsd:string` | Sì | Stringa di definizione. Vedere di seguito. |

**Output (setAssetSetDefinitionReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## setDefinition Parameter: Informazioni su {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition Functions**

Specificare le funzioni di sostituzione `setDefinition` in linea. Questi problemi vengono risolti durante la ricerca di un catalogo o durante la pubblicazione. Le stringhe di sostituzione hanno il formato `${<substitution_func>}` e includono quanto segue:

>[!NOTE]
>
>I valori letterali delle maniglie negli elenchi dei parametri devono essere racchiusi tra parentesi quadre `([])`. Il testo all&#39;esterno di una stringa di sostituzione viene copiato nella stringa di output durante la risoluzione.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Funzione di sostituzione </th> 
   <th colname="col2" class="entry"> Restituisce la risorsa </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> Percorso del file principale. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> ID catalogo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([  <span class="varname"> asset_handle  </span>],[  <span class="varname"> metadata_field_handle  </span>])  </span> </td> 
   <td colname="col2"> Valore metadati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> ID catalogo. Si applica alle risorse basate su immagini (Immagine, Vista regolata, Visualizzazione livello). <p>Per le altre risorse, restituisce l’ID del catalogo della risorsa miniatura (se presente). Se alla risorsa non è associata alcuna risorsa miniatura, la funzione restituisce una stringa vuota. </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition Examples**

Stringa di definizione del set di file multimediali:

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

In fase di ricerca o pubblicazione viene risolto quanto segue:

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Esempi {#section-739b42eec3074cafae285ec015a2d088}

**Request Contents (Richiesta contenuto)**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**Risposta**

Nessuno.
