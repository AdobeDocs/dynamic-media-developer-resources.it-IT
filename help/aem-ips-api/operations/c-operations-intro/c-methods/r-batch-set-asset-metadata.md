---
description: Imposta i metadati delle risorse utilizzando la modalità batch.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 12%

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
| companyHandle | `xsd:string` | Sì | L&#39;handle dell&#39;azienda di cui si desidera impostare i metadati in un&#39;operazione batch. |
| updateArray | `types:BatchMetadataUpdateArray` | Sì | Array di aggiornamenti di metadati applicati alle risorse. |

**Output (batchSetAssetMetadataParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di metadati impostati correttamente. |
| warningCount | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di impostare i metadati. |
| errorCount | `xsd:int` | Sì | Il numero di errori generati quando l&#39;operazione tentava di impostare i metadati. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generano avvisi quando l’operazione tentava di impostare in batch i metadati per le risorse. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generano errori quando l’operazione tentava di impostare in batch i metadati per le risorse. |

## Esempi {#section-2de798ac920e4b47b971b1729a64395b}

**Request Contents (Richiesta contenuto)**

```java {.line-numbers}
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

```java {.line-numbers}
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
