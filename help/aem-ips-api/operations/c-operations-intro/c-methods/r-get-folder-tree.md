---
description: Restituisce cartelle e sottocartelle in una struttura ad albero gerarchica. La risposta getFolderTree è limitata a un massimo di 100.000 cartelle
seo-description: Restituisce cartelle e sottocartelle in una struttura ad albero gerarchica. La risposta getFolderTree è limitata a un massimo di 100.000 cartelle
seo-title: getFolderTree
solution: Experience Manager
title: getFolderTree
topic: Scene7 Image Production System API
uuid: 93fda0d6-c656-4254-b07b-7a448e164f28
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
>L&#39;utente deve disporre dell&#39;accesso in lettura alla cartella per restituire i dati in essa contenuti.

## Parametri {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Input (getFolderTreeParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società. |
| ` *`accessUserHandle`*` | `xsd:string` | No | Utilizzata solo dagli amministratori per rappresentare un utente specifico. |
| ` *`accessGroupHandle`*` | `xsd:string` | No | Utilizzato per filtrare in base a uno specifico gruppo, compresi quelli a cui appartiene la società. |
| ` *`folderPath`*` | `xsd:string` | No | Cartella principale per recuperare le cartelle e tutte le sottocartelle al livello foglia. Se esclusa, viene utilizzata la radice della società. |
| ` *`profondità`*` | `xsd:int` | Sì | Con un valore pari a zero si ottiene la cartella di livello principale. Qualsiasi altro valore specifica la profondità da scendere nella struttura ad albero. |
| ` *`assetTypeArray`*` | `types:StringArray` | No | Restituisce cartelle contenenti solo tipi di risorse specificati. |
| ` *`responseFieldArray`*` | `types:StringArray` | No | Contiene un elenco di campi che si desidera includere nella risposta. |
| ` *`excludeFieldArray`*` | `types:StringArray` | No | Contiene un elenco di campi da escludere nella risposta. |

**Output (getFolderTreeReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`folder`*` | `types:folders` | No | La gerarchia di cartelle in una struttura ad albero. La risposta è limitata a un massimo di 100.000 cartelle. |
| ` *`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## Esempi {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

Questo esempio di codice utilizza un handle della società e un parametro di profondità per determinare il livello di profondità che la risposta deve restituire. La risposta contiene le cartelle e gli array di sottocartelle correlati. Impostate il valore di profondità su un numero minore per eseguire ricerche più approfondite nella struttura delle cartelle.

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

