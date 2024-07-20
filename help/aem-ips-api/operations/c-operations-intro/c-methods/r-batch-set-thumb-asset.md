---
description: Imposta l'immagine di anteprima per una o più risorse.
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 9%

---

# batchSetThumbAsset{#batchsetthumbasset}

Imposta l&#39;immagine di anteprima per una o più risorse.

Sintassi

## Tipi di risorse miniature {#section-4edc2a6a8f824213b0aaddb1d437268c}

I tipi di risorse miniature consentiti sono i seguenti:

* Immagine
* AdjustedView
* Maschera
* Modello
* PsdTemplate

## Tipi di utenti autorizzati {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura/scrittura alla risorsa di destinazione e dell’accesso in lettura alla risorsa miniatura.

## Parametri {#section-9c6efa000b384b3db6c013def20cf40b}

**Input (batchSetThumbAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell’azienda contenente le risorse. |
| updateArray | `types:ThumbAssetUpdateArray` | Sì | Array di aggiornamenti. |

**Output (batchSetThumbAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di miniature impostate correttamente. |
| warningCount | `xsd:int` | Sì | Numero di avvisi generati quando si è tentato di impostare le miniature. |
| errorCount | `xsd:int` | Sì | Il numero di errori generati quando l&#39;operazione ha tentato di impostare le miniature. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione ha tentato di applicare gli aggiornamenti. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | L’array di dettagli associati alle risorse che hanno generato errori quando l’operazione ha tentato di applicare gli aggiornamenti. |

## Esempi {#section-6de69a8680c24c1486c5f01488393381}

**Richiesta**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**Risposta**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```
