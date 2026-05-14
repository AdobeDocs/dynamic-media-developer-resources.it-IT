---
description: Sposta una cartella in una nuova posizione.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa31c2d8-912c-4965-8535-cae42f4fcfd9
TQID: 'https://experienceleague.adobe.com/xnBMdEtQN9m8JZZNfa8mPR1Zl6XyS-zYwM5JJzPREv0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 60
ht-degree: 20%

---

# moveFolder{#movefolder}

Sposta una cartella in una nuova posizione.

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
| companyHandle | `xsd:string` | Sì | Gestire l&#39;azienda. |
| folderHandle | `xsd:string` | Sì | Handle di cartella. |
| destFolderHandle | `xsd:string` | Sì | Gestisci fino alla cartella di destinazione. |

**Output (moveFolderReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| folderHandle | `xsd:string` | Sì | Gestisci la cartella spostata. |

## Esempi {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Richiesta**

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
