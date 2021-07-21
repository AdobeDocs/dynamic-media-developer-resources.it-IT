---
description: Spostare una cartella in un nuovo percorso.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 23%

---

# moveFolder{#movefolder}

Spostare una cartella in un nuovo percorso.

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
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`folderHandle`*` | `xsd:string` | Sì | Maniglia della cartella. |
| `*`destFolderHandle`*` | `xsd:string` | Sì | Gestisci la cartella di destinazione. |

**Output (moveFolderReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Sì | Gestisci la cartella spostata. |

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
