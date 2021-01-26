---
description: Imposta campi specifici per un’immagine per una o più risorse di immagine.
seo-description: Imposta campi specifici per un’immagine per una o più risorse di immagine.
seo-title: batchSetImageFields
solution: Experience Manager
title: batchSetImageFields
topic: Dynamic Media Image Production System API
uuid: e0ad7da4-cb28-4402-8b47-a600916d23b3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 8%

---


# batchSetImageFields{#batchsetimagefields}

Imposta campi specifici per un’immagine per una o più risorse di immagine.

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
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle della società che contiene le risorse immagine. |
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | Sì | L’array di aggiornamenti dei campi immagine. |

**Output (batchSetImageFields)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di campi immagine impostati correttamente. |
| `*`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di impostare i campi immagine. |
| `*`errorCount`*` | `xsd:int` | Sì | Numero di errori generati quando l&#39;operazione tentava di impostare i campi immagine. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano avvisi quando l&#39;operazione tentava di applicare gli aggiornamenti. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano errori quando l&#39;operazione tentava di applicare gli aggiornamenti. |

## Esempi {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Questo esempio imposta i dati nei campi di due immagini in un array di aggiornamento. Nell’array, le immagini sono specificate dalle relative maniglie della risorsa e contengono risoluzione in pixel, coordinate di ancoraggio per posizioni x e y e dati utente. La risposta indica che i campi per entrambe le immagini sono stati impostati correttamente.

**Request Contents (Richiesta contenuto)**

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

