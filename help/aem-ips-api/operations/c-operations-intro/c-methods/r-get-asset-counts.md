---
description: Ottiene le risorse e il numero di risorse associate a una società specifica.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 8%

---


# getAssetCounts{#getassetcounts}

Ottiene le risorse e il numero di risorse associate a una società specifica.

Il `countArray` restituito è costituito da una matrice di `assetTypes` (tipo di dati `xsd:string`), ciascuna con il proprio campo conteggio (tipo di dati `xsd:int`), che consente la rappresentazione di più tipi di risorse per elemento della matrice.
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
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda con le risorse che desideri conteggiare. |

**Output (getAssetCountsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | No | Matrice di tipi di risorse, ciascuno con un proprio campo di conteggio, che consente la rappresentazione di più tipi di risorse per elemento dell’array. |

## Esempi {#section-6052a503eb3843f6adb99e200fdba280}

Questo esempio di codice utilizza l’handle dell’azienda come campo nel `getAssetCountsParam` inviato al server dei servizi Web IPS per ottenere i conteggi delle risorse.

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

