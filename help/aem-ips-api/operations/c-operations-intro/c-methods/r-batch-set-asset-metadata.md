---
description: Imposta i metadati delle risorse utilizzando la modalità batch.
seo-description: Imposta i metadati delle risorse utilizzando la modalità batch.
seo-title: batchSetAssetMetadata
solution: Experience Manager
title: batchSetAssetMetadata
topic: Scene7 Image Production System API
uuid: 88d8f279-988f-4956-b66f-60fa95cf511c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 11%

---


# batchSetAssetMetadata{#batchsetassetmetadata}

Imposta i metadati delle risorse utilizzando la modalità batch.

Sintassi

## Tipi di utenti autorizzati {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-7111ac93bc7747f69ba14db4ac3912b0}

**Input (batchSetAssetMetadataParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società di cui si desidera impostare i metadati in un’operazione batch. |
| ` *`updateArray`*` | `types:BatchMetadataUpdateArray` | Sì | Array di aggiornamenti di metadati applicati alle risorse. |

**Output (batchSetAssetMetadataParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sì | Numero di metadati impostati correttamente. |
| ` *`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di impostare i metadati. |
| ` *`errorCount`*` | `xsd:int` | Sì | Numero di errori generati quando l&#39;operazione tentava di impostare i metadati. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | L’array di dettagli associati alle risorse che generano avvisi quando l’operazione tenta di impostare in batch i metadati per le risorse. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | L’array di dettagli associati alle risorse che generano errori quando l’operazione tentava di impostare in batch i metadati per le risorse. |

## Esempi {#section-2de798ac920e4b47b971b1729a64395b}

**Request Contents (Richiesta contenuto)**

```java
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**Risposta**

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

