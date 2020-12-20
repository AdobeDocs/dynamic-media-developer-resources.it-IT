---
description: Spostate una cartella in un nuovo percorso.
seo-description: Spostate una cartella in un nuovo percorso.
seo-title: moveFolder
solution: Experience Manager
title: moveFolder
topic: Scene7 Image Production System API
uuid: 424858c3-5796-4ae9-b5ad-fd50ddbee702
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 22%

---


# moveFolder{#movefolder}

Spostate una cartella in un nuovo percorso.

Sintassi

## Tipi di utenti autorizzati {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Input (moveFolderParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Gestite l&#39;azienda. |
| ` *`folderHandle`*` | `xsd:string` | Sì | handle della cartella. |
| ` *`destFolderHandle`*` | `xsd:string` | Sì | Consente di passare alla cartella di destinazione. |

**Output (moveFolderReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Sì | Consente di passare alla cartella spostata. |

## Esempi {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Request Contents (Richiesta contenuto)**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**Risposta**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

