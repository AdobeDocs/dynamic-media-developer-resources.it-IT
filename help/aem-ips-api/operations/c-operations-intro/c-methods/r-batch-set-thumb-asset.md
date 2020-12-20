---
description: Imposta la miniatura di una o più risorse.
seo-description: Imposta la miniatura di una o più risorse.
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
topic: Scene7 Image Production System API
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# batchSetThumbAsset{#batchsetthumbasset}

Imposta la miniatura di una o più risorse.

Sintassi

## Tipi di risorse miniatura {#section-4edc2a6a8f824213b0aaddb1d437268c}

I tipi di risorse in miniatura consentiti sono i seguenti:

* Immagine
* Visualizz. modific.
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
>L’utente deve disporre dell’accesso in lettura/scrittura alla risorsa di destinazione e accedere in lettura alla risorsa della miniatura.

## Parametri {#section-9c6efa000b384b3db6c013def20cf40b}

**Input (batchSetThumbAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società che contiene le risorse. |
| ` *`updateArray`*` | `types:ThumbAssetUpdateArray` | Sì | Array di aggiornamenti. |

**Output (batchSetThumbAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sì | Numero di miniature impostate correttamente. |
| ` *`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di impostare le miniature. |
| ` *`errorCount`*` | `xsd:int` | Sì | Numero di errori generati quando l&#39;operazione tentava di impostare le miniature. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano avvisi quando l&#39;operazione tentava di applicare gli aggiornamenti. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano errori quando l&#39;operazione tentava di applicare gli aggiornamenti. |

## Esempi {#section-6de69a8680c24c1486c5f01488393381}

**Request Contents (Richiesta contenuto)**

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

