---
description: Sposta più risorse in modo indipendente l’una dall’altra. A tale scopo, utilizza il tipo AssetMove contenuto in assetMoveArray. Ogni campo AssetMove contiene una cartella di destinazione.
solution: Experience Manager
title: moveAssets
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Developer,Administrator
exl-id: e5bb2188-d262-4324-9f71-68634b6af654
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 8%

---

# moveAssets{#moveassets}

Sposta più risorse in modo indipendente l’una dall’altra. A tale scopo, utilizza il tipo AssetMove contenuto in assetMoveArray. Ogni campo AssetMove contiene una cartella di destinazione.

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
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda con risorse da spostare. |
| `*`assetMoveArray`*` | `types:AssetMoveArray` | Sì | Matrice per lo spostamento delle risorse. Contiene una risorsa e una cartella di destinazione della risorsa. |

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Il conteggio delle risorse è stato spostato. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Numero di risorse che hanno generato avvisi quando l’operazione tentava di spostarle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Numero di risorse che hanno generato errori quando l’operazione tentava di spostarle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <span class="codeph"> </span>AssetOperationFaults che contengono: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Risorse che hanno generato gli avvisi. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Codici di avvertenza. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Motivo dell'avviso. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <span class="codeph"> </span>AssetOperationFaults che contengono: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Risorse che hanno generato gli errori. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Codici di errore. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Motivo degli errori. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Esempi {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Questo codice di esempio sposta le risorse in una posizione specifica specificata da `assetMoveArray`. L’array include la maniglia della risorsa e il relativo handle di cartella. La risposta indica che le risorse sono state spostate correttamente.

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
