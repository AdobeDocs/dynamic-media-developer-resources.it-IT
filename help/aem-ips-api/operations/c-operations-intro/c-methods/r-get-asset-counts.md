---
description: Ottiene i cespiti e il numero di cespiti associati a una società specifica.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '141'
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
