---
description: Ripristina le risorse dal cestino.
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 10%

---


# restoreAssetsFromTrash{#restoreassetsfromtrash}

Ripristina le risorse dal cestino.

Sintassi

## Tipi di utenti autorizzati {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-200a61d040c94e489a85241b29cd499a}

**Input (restoreAssetsFromTrashParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle di una società con le risorse da ripristinare. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sì | Array di handle per le risorse da ripristinare. |

**Output (restoreAssetsFromTrashReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di risorse rimosse dal cestino. |
| `*`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l’operazione tentava di ripristinare le risorse dal cestino. |
| `*`errorCount`*` | `xsd:int` | Sì | Numero di errori generati durante il tentativo di ripristinare le risorse dal cestino. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione tentava di ripristinare le risorse dal cestino. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato errori quando l’operazione tentava di ripristinare le risorse dal cestino. |

## Esempi {#section-98fe0394b0634ca397c395f14f8a9358}

Questo esempio di codice ripristina le risorse dal cestino. La risposta indica che l’operazione è stata completata correttamente.

**Request Contents (Richiesta contenuto)**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Risposta**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```

