---
description: Rimuove le risorse da un progetto. Non distrugge le risorse.
seo-description: Rimuove le risorse da un progetto. Non distrugge le risorse.
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
topic: Scene7 Image Production System API
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# removeProjectAssets{#removeprojectassets}

Rimuove le risorse da un progetto. Non distrugge le risorse.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con le risorse da spostare. |
| ` *`projectHandle`*` | `xsd:string` | Sì | L’handle delle risorse del progetto da spostare. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Sì | Array di handle per le risorse da spostare. |

**Output (removeProjectAssetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sì | È stato rimosso il conteggio delle risorse. |
| ` *`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di rimuovere le risorse dal progetto. |
| ` *`errorCount`*` | `xsd:int` | Sì | Il numero di errori generati quando l&#39;operazione tentava di rimuovere le risorse dal progetto. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano avvisi quando l&#39;operazione tentava di rimuoverli dal progetto. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | L&#39;array di dettagli associati alle risorse che generavano errori quando l&#39;operazione tentava di rimuoverli dal progetto. |

## Esempi {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Questo esempio di codice rimuove 2 risorse da un progetto (specificato dall’handle del progetto).

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

