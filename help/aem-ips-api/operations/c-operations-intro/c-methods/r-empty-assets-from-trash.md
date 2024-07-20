---
title: emptyAssetsFromTrash
description: Svuota le risorse dal cestino IPS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 5%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Svuota le risorse dal cestino IPS.

Assets vive nel cestino finché non viene svuotato manualmente o finché non esce dal cestino. Se vengono svuotati manualmente, vivono nel Cestino fino al successivo lavoro di pulizia (normalmente notturno), quando vengono infine eliminati dal sistema. Se escono dal cestino, le risorse vengono pulite come parte della stessa attività di pulizia. Il timeout è configurabile (l’impostazione predefinita è 7 giorni).

## Tipi di utenti autorizzati {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-8e1fb0ee3aae453581e99ef76e298569}

**Input (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | xsd:stringa | Sì | Handle per l&#39;azienda proprietaria delle risorse. |
| assetHandleArray | tipi:HandleArray | Sì | Array di handle che rappresentano gli elementi da svuotare dal cestino. |

**Output (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | xsd:Int | Sì | Numero di risorse svuotate dal cestino. |
| warningCount | xsd:Int | Sì | Numero di avvisi generati quando l’operazione ha tentato di svuotare le risorse dal cestino. |
| errorCount | xsd:Int | Sì | Numero di errori generati quando l’operazione ha tentato di svuotare le risorse dal cestino. |
| warningDetailArray | tipi:AssetOperationFaultArray | No | Matrice di dettagli associata alle risorse che hanno generato avvisi quando l’operazione ha tentato di svuotarle dal cestino. |
| errorDetailArray | tipi:AssetOperationFaultArray | No | Array di dettagli associati alle risorse che hanno generato errori quando l’operazione ha tentato di svuotarle dal cestino. |

## Esempi {#section-6154a873b6c342bf92e2036280cafdcf}

In questo esempio di codice vengono utilizzati l&#39;handle della società e un array di handle di risorsa contenente gli handle delle risorse da svuotare dal cestino.

**Richiesta**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Risposta**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
