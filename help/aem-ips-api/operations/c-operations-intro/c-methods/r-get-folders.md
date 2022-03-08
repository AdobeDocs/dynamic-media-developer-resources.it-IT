---
description: Restituisce tutte le cartelle e le sottocartelle, a partire dal percorso della cartella. La risposta getFolders restituisce un massimo di 100.000 cartelle.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 8%

---

# getFolders{#getfolders}

Restituisce tutte le cartelle e le sottocartelle, a partire dal percorso della cartella. La risposta getFolders restituisce un massimo di 100.000 cartelle.

## Scopo delle cartelle {#section-66e344d5333f42f1b060a0cba25935c3}

Una cartella consente di organizzare sottocartelle e risorse. Tutti i nomi delle cartelle e delle risorse devono essere univoci. Le cartelle e le risorse che condividono lo stesso nome causano un conflitto di namespace, anche se si trovano in gerarchie di cartelle diverse.
Sintassi

## Tipi di utenti autorizzati {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Per restituire i dati contenuti nella cartella, l’utente deve disporre dell’accesso in lettura.

## Parametri {#section-0c1976503eaa418a9226b51667901176}

**Input (getFoldersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Il manico per l&#39;azienda. |
| accessUserHandle | `xsd:string` | No | Utilizzato dagli amministratori per rappresentare un utente specifico. |
| accessGroupHandle | `xsd:string` | No | Filtrare per un gruppo specifico. |
| folderPath | `xsd:string` | No | Cartella principale per recuperare cartelle e sottocartelle a livello foglia. Se viene esclusa, viene utilizzata la radice della società. |
| assetTypeArray | `types:StringArray` | No | Restituisce cartelle che contengono solo tipi di risorse specificati. |
| responseFieldArray | `types:StringArray` | No | Contiene un elenco di campi che si desidera includere nella risposta. |
| excludeFieldArray | `types:StringArray` | No | Contiene un elenco di campi da escludere dalla risposta. |

**Output (getFoldersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| folderArray | `types:FolderArray` | No | Matrice di cartelle corrispondenti ai criteri del filtro. La risposta è limitata a un massimo di 100.000 cartelle. |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## Esempi {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Questo esempio di codice restituisce un array contenente tutte le cartelle di un&#39;azienda insieme a informazioni specifiche su ciascuna cartella.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**Risposta**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```
