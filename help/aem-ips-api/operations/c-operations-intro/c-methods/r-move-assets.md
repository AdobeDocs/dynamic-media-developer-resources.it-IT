---
description: Sposta più risorse indipendentemente l'una dall'altra. A questo scopo, utilizza il tipo AssetMove contenuto in assetMoveArray. Ogni campo AssetMove contiene una cartella di destinazione.
seo-description: Sposta più risorse indipendentemente l'una dall'altra. A questo scopo, utilizza il tipo AssetMove contenuto in assetMoveArray. Ogni campo AssetMove contiene una cartella di destinazione.
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Scene7 Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAssets{#moveassets}

Sposta più risorse indipendentemente l&#39;una dall&#39;altra. A questo scopo, utilizza il tipo AssetMove contenuto in assetMoveArray. Ogni campo AssetMove contiene una cartella di destinazione.

Sintassi

## Tipi di utenti autorizzati {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-7d47f663474b41cc83439288ac133cc5}

**Input (moveAssetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con le risorse da spostare. |
| ` *`assetMoveArray`*` | `types:AssetMoveArray` | Sì | Un array di spostamento risorse. Contiene una risorsa e una cartella di destinazione. |

**Output (moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Il conteggio delle risorse è stato spostato correttamente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Conteggio delle risorse che generavano avvisi quando l'operazione tentava di spostarle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Conteggio delle risorse che generavano errori quando l'operazione tentava di spostarle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaultsche contengono:</span> 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Risorse per la generazione degli avvisi. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Codici di avvertenza. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Motivo dell’avviso. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> errorDetailArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaultsche contengono:</span> 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Risorse che hanno generato gli errori. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Codici di errore. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Motivo degli errori. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Questo esempio di codice sposta le risorse in una posizione specifica specificata dall’ `assetMoveArray`. L’array include la maniglia della risorsa e la relativa maniglia della cartella. La risposta indica che le risorse sono state spostate correttamente.

**Request Contents (Richiesta contenuto)**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**Risposta**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

