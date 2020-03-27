---
description: Elimina le risorse dal cestino IPS.
seo-description: Elimina le risorse dal cestino IPS.
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Scene7 Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

Elimina le risorse dal cestino IPS.

Le risorse vivono nel cestino fino a quando non vengono svuotate manualmente o fino a quando non escono dal cestino. Se vengono svuotati manualmente, vivono nel Cestino fino al successivo processo di pulizia (normalmente notturno) quando vengono infine eliminati dal sistema. Se non vengono utilizzati, le risorse vengono eliminate come parte della stessa attività di pulizia. Il timeout è configurabile (il valore predefinito è 7 giorni).

## Tipi di utenti autorizzati {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* ``

## Parametri {#section-8e1fb0ee3aae453581e99ef76e298569}

**Input (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società proprietaria delle risorse. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Sì | Array di handle che rappresentano gli elementi da svuotare dal cestino. |

**Output (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`successCount`*` | `xsd:Int` | Sì | Numero di risorse svuotate correttamente dal cestino. |
| ` *`warningCount`*` | `xsd:Int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di svuotare le risorse dal cestino. |
| ` *`errorCount`*` | `xsd:Int` | Sì | Numero di errori generati quando l&#39;operazione tentava di svuotare le risorse dal cestino. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano avvisi quando l&#39;operazione tentava di svuotarle dal cestino. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano errori quando l&#39;operazione tentava di svuotarle dal cestino. |

## Esempi {#section-6154a873b6c342bf92e2036280cafdcf}

In questo esempio di codice vengono utilizzati l’handle della società e un array di handle della risorsa che contiene le maniglie per le risorse da svuotare dal cestino.

**Request Contents (Richiesta contenuto)**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Risposta**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

