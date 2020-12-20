---
description: Ottiene le risorse e il numero di risorse associate a una società specifica.
seo-description: Ottiene le risorse e il numero di risorse associate a una società specifica.
seo-title: getAssetCount
solution: Experience Manager
title: getAssetCount
topic: Scene7 Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 8%

---


# getAssetCount{#getassetcounts}

Ottiene le risorse e il numero di risorse associate a una società specifica.

La `countArray` restituita è costituita da un array di `assetTypes` (tipo di dati `xsd:string`), ciascuno con un proprio campo di conteggio (tipo di dati `xsd:int`), che consente la rappresentazione di più tipi di risorse per elemento dell&#39;array.
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

**Input (getAssetCountParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con le risorse da conteggiare. |

**Output (getAssetCountsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`countArray`*` | `types:AssetCountArray` | No | Un array di tipi di risorse, ciascuno con un proprio campo di conteggio, che consente la rappresentazione di più tipi di risorse per elemento dell’array. |

## Esempi {#section-6052a503eb3843f6adb99e200fdba280}

Questo esempio di codice utilizza l&#39;handle della società come campo nel `getAssetCountsParam` inviato al server dei servizi Web IPS per ottenere i conteggi delle risorse.

**Request Contents (Richiesta contenuto)**

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

