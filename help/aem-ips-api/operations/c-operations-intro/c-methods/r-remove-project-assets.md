---
description: Rimuove risorse da un progetto. Non distrugge le risorse.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 8%

---

# removeProjectAssets{#removeprojectassets}

Rimuove risorse da un progetto. Non distrugge le risorse.

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
| companyHandle | `xsd:string` | Sì | Handle dell’azienda con le risorse da spostare. |
| projectHandle | `xsd:string` | Sì | Handle delle risorse del progetto da spostare. |
| assetHandleArray | `types:HandleArray` | Sì | Array di handle per le risorse da spostare. |

**Output (removeProjectAssetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Il conteggio delle risorse è stato rimosso. |
| warningCount | `xsd:int` | Sì | Numero di avvisi generati quando l’operazione ha tentato di rimuovere risorse dal progetto. |
| errorCount | `xsd:int` | Sì | Il numero di errori generati quando l’operazione ha tentato di rimuovere risorse dal progetto. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione ha tentato di rimuoverle dal progetto. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato errori quando l’operazione ha tentato di rimuoverle dal progetto. |

## Esempi {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

In questo esempio di codice vengono rimosse 2 risorse da un progetto (specificato dall&#39;handle del progetto).

**Richiesta**

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
