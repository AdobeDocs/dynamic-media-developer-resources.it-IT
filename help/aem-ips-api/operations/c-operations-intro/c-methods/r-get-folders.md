---
description: Restituisce tutte le cartelle e sottocartelle, a partire dal percorso della cartella. La risposta getFolders restituisce un massimo di 100.000 cartelle.
seo-description: Restituisce tutte le cartelle e sottocartelle, a partire dal percorso della cartella. La risposta getFolders restituisce un massimo di 100.000 cartelle.
seo-title: getFolders
solution: Experience Manager
title: getFolders
topic: Dynamic Media Image Production System API
uuid: 06e9d745-b711-43e3-8dc6-93da66b981b1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 7%

---


# getFolders{#getfolders}

Restituisce tutte le cartelle e sottocartelle, a partire dal percorso della cartella. La risposta getFolders restituisce un massimo di 100.000 cartelle.

## Finalità delle cartelle {#section-66e344d5333f42f1b060a0cba25935c3}

Una cartella consente di organizzare sottocartelle e risorse. Tutti i nomi delle cartelle e delle risorse devono essere univoci. Le cartelle e le risorse che condividono lo stesso nome causeranno un conflitto di nomi, anche se si trovano in gerarchie di cartelle diverse.
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
>L&#39;utente deve disporre dell&#39;accesso in lettura alla cartella per restituire i dati in essa contenuti.

## Parametri {#section-0c1976503eaa418a9226b51667901176}

**Input (getFoldersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società. |
| `*`accessUserHandle`*` | `xsd:string` | No | Utilizzato dagli amministratori per rappresentare un utente specifico. |
| `*`accessGroupHandle`*` | `xsd:string` | No | Filtrare per un gruppo specifico. |
| `*`folderPath`*` | `xsd:string` | No | Cartella principale per recuperare le cartelle e tutte le sottocartelle al livello foglia. Se esclusa, viene utilizzata la radice della società. |
| `*`assetTypeArray`*` | `types:StringArray` | No | Restituisce cartelle contenenti solo tipi di risorse specificati. |
| `*`responseFieldArray`*` | `types:StringArray` | No | Contiene un elenco di campi che si desidera includere nella risposta. |
| `*`excludeFieldArray`*` | `types:StringArray` | No | Contiene un elenco di campi da escludere dalla risposta. |

**Output (getFoldersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | No | Un array di cartelle che corrispondono ai criteri del filtro. La risposta è limitata a un massimo di 100.000 cartelle. |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## Esempi {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Questo esempio di codice restituisce un array che contiene tutte le cartelle di una società insieme a informazioni specifiche su ciascuna cartella.

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

