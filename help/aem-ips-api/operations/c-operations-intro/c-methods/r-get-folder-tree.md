---
description: Restituisce cartelle e sottocartelle in una struttura ad albero gerarchica. La risposta getFolderTree è limitata a un massimo di 100.000 cartelle
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 7%

---

# getFolderTree{#getfoldertree}

Restituisce cartelle e sottocartelle in una struttura ad albero gerarchica. La risposta getFolderTree è limitata a un massimo di 100.000 cartelle

Sintassi

## Tipi di utenti autorizzati {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Per restituire i dati contenuti nella cartella, l’utente deve disporre dell’accesso in lettura.

## Parametri {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Input (getFolderTreeParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Il manico per l&#39;azienda. |
| `*`accessUserHandle`*` | `xsd:string` | No | Utilizzato solo dagli amministratori per rappresentare un utente specifico. |
| `*`accessGroupHandle`*` | `xsd:string` | No | Utilizzato per filtrare in base a un gruppo specifico, compresi quelli a cui appartiene la società. |
| `*`folderPath`*` | `xsd:string` | No | Cartella principale per recuperare cartelle e sottocartelle a livello foglia. Se viene esclusa, viene utilizzata la radice della società. |
| `*`profondità`*` | `xsd:int` | Sì | Il valore zero restituisce la cartella di livello superiore. Qualsiasi altro valore specifica la profondità da scendere nell&#39;albero. |
| `*`assetTypeArray`*` | `types:StringArray` | No | Restituisce cartelle che contengono solo tipi di risorse specificati. |
| `*`responseFieldArray`*` | `types:StringArray` | No | Contiene un elenco di campi che si desidera includere nella risposta. |
| `*`excludeFieldArray`*` | `types:StringArray` | No | Contiene un elenco di campi da escludere nella risposta. |

**Output (getFolderTreeReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`cartelle`*` | `types:folders` | No | La gerarchia delle cartelle in una struttura ad albero. La risposta è limitata a un massimo di 100.000 cartelle. |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## Esempi {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

Questo esempio di codice utilizza un handle aziendale e un parametro di profondità per determinare il livello di profondità che la risposta deve restituire. La risposta contiene cartelle e array di sottocartelle correlati. Imposta il valore di profondità su un numero più piccolo per cercare più in profondità nella struttura delle cartelle.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**Risposta**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```
