---
description: Assegna o aggiorna le risorse in un progetto.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
TQID: 'https://experienceleague.adobe.com/J5X6PS7L7YCH6J9ClzAUo24O44fMWxNqPnILckRBbUI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 14%

---

# setProjectAssets{#setprojectassets}

Assegna o aggiorna le risorse in un progetto.

Sintassi

## Tipi di utenti autorizzati {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Input (setProjectAssetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyName | `xsd:string` | Sì | Gestore azienda. |
| projectHandle | `xsd:string` | Sì | Handle di progetto. |
| assetHandleArray | `types:HandleArray` | Sì | Matrice di handle di risorsa da associare al progetto. |

**Output (setProjectAssetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di risorse aggiunte correttamente. |

## Esempi {#section-33c1a909c3dc4aa98da474c23a036596}

Questo esempio di codice assegna una risorsa a un progetto. La richiesta restituisce un numero di operazioni riuscite pari a uno.

**Richiesta**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Risposta**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```
