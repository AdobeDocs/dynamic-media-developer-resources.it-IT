---
description: Imposta campi specifici per l’immagine per una o più risorse immagine.
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 7%

---

# batchSetImageFields{#batchsetimagefields}

Imposta campi specifici per l’immagine per una o più risorse immagine.

Sintassi

## Tipi di utenti autorizzati {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-4969815cf67c4d11b13bb2017b3604e8}

**Input (batchSetImageFields)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle della società che contiene le risorse immagine. |
| updateArray | `types:ImageFieldUpdateArray` | Sì | L’array di aggiornamenti dei campi immagine. |

**Output (batchSetImageFields)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di campi immagine impostati correttamente. |
| warningCount | `xsd:int` | Sì | Il numero di avvisi generati quando l’operazione ha tentato di impostare i campi immagine. |
| errorCount | `xsd:int` | Sì | Il numero di errori generati quando l’operazione ha tentato di impostare i campi immagine. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione ha tentato di applicare gli aggiornamenti. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | L’array di dettagli associati alle risorse che hanno generato errori quando l’operazione ha tentato di applicare gli aggiornamenti. |

## Esempi {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Questo esempio imposta i dati nei campi di due immagini in un array di aggiornamento. Nell’array, le immagini sono specificate dai relativi handle di risorsa e contengono la risoluzione in pixel, le coordinate di ancoraggio della posizione x e y e i dati utente. La risposta indica che i campi per entrambe le immagini sono stati impostati correttamente.

**Richiesta**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**Risposta**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```
