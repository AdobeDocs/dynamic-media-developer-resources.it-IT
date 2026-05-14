---
description: Ottiene i cespiti e il numero di cespiti associati a una società specifica.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
TQID: 'https://experienceleague.adobe.com/gvFs-dqQ8oR38MTKrEYaap31BH-MtSaRtGtJd5FO-MY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 7%

---

# getAssetCounts{#getassetcounts}

Ottiene i cespiti e il numero di cespiti associati a una società specifica.

Il `countArray` restituito è costituito da un array di `assetTypes` (tipo di dati `xsd:string`), ciascuno con un proprio campo di conteggio (tipo di dati `xsd:int`), che consente la rappresentazione di più tipi di risorse per elemento dell&#39;array.
Sintassi

## Tipi di utenti autorizzati {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**Input (getAssetCountsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell’azienda con le risorse da conteggiare. |

**Output (getAssetCountsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| countArray | `types:AssetCountArray` | No | Matrice di tipi di risorse, ciascuno con un proprio campo di conteggio, che consente la rappresentazione di più tipi di risorse per elemento della matrice. |

## Esempi {#section-6052a503eb3843f6adb99e200fdba280}

In questo esempio di codice viene utilizzato l&#39;handle della società come campo in `getAssetCountsParam` inviato al server dei servizi Web IPS per ottenere il numero di risorse.

**Richiesta**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**Risposta**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```
