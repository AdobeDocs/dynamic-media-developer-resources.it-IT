---
title: emptyAssetsFromTrash
description: Svuota le risorse dal cestino IPS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
TQID: 'https://experienceleague.adobe.com/y-TOHfExSc5RL9-j0f-pU6uKXWuSKSrn9SG7w0e5jPg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 252
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
| companyHandle | xsd:string | Sì | Handle per l&#39;azienda proprietaria delle risorse. |
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
