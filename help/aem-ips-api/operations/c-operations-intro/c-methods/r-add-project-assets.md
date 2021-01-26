---
description: Aggiunge una o più risorse a un progetto.
solution: Experience Manager
title: addProjectAssets
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 10%

---


# addProjectAssets{#addprojectassets}

Aggiunge una o più risorse a un progetto.

Sintassi

## Tipi di utenti autorizzati {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-20d498e971b6466298e60c8a77fc32b2}

**Input (addProjectAssetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Gestire la società associata al progetto corrente. |
| `*`projectHandle`*` | `xsd:string` | Sì | Gestite il progetto al quale state aggiungendo delle risorse. |
| `*`projectHandleArray`*` | `xsd:HandleArray` | Sì | Array di risorse che state aggiungendo al progetto corrente. |

**Output (addProjectAssetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di risorse aggiunte correttamente. |
| `*`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di aggiungere risorse a un progetto. |
| `*`errorCount`*` | `xsd:int` | Sì | Il numero di errori generati quando l&#39;operazione tentava di aggiungere risorse a un progetto. |
| `*`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | No | Array di avvisi generati dalle risorse quando l&#39;operazione tentava di aggiungerli a un progetto. |
| `*`companyHandle`*` | `xsd:AssetOperationFaultArray` | No | Array di errori generati dalle risorse quando l&#39;operazione tentava di aggiungerli a un progetto. |

## Esempi {#section-bee5be2402f54cb9a3a02cc07def4135}

In questo esempio viene aggiunta una singola risorsa (a cui fa riferimento il relativo handle) in un array di handle di risorsa a un progetto specificato nella richiesta. Operazione completata correttamente quando la risposta `successCount` restituisce `1`.

**Request Contents (Richiesta contenuto)**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Risposta**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

