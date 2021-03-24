---
description: Rimuove le risorse da un progetto. Non distrugge i beni.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 9%

---


# removeProjectAssets{#removeprojectassets}

Rimuove le risorse da un progetto. Non distrugge i beni.

Sintassi

## Tipi di utenti autorizzati {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-169d8e317417415b87df86242f65710e}

**Input (removeProjectAssetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda con le risorse da spostare. |
| `*`projectHandle`*` | `xsd:string` | Sì | L’handle delle risorse del progetto da spostare. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sì | Matrice di handle per le risorse da spostare. |

**Output (removeProjectAssetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Il conteggio delle risorse è stato rimosso. |
| `*`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l’operazione tentava di rimuovere risorse dal progetto. |
| `*`errorCount`*` | `xsd:int` | Sì | Il numero di errori generati quando l’operazione tentava di rimuovere le risorse dal progetto. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione tentava di rimuoverli dal progetto. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matrice di dettagli associati alle risorse che generavano errori quando l’operazione tentava di rimuoverli dal progetto. |

## Esempi {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Questo esempio di codice rimuove 2 risorse da un progetto (specificato dalla gestione del progetto).

**Request Contents (Richiesta contenuto)**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```

