---
description: Imposta campi specifici per le immagini per una o più risorse di immagini.
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 9%

---

# batchSetImageFields{#batchsetimagefields}

Imposta campi specifici per le immagini per una o più risorse di immagini.

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
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | Sì | La matrice dei campi immagine viene aggiornata. |

**Output (batchSetImageFields)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di campi immagine impostati correttamente. |
| `*`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l’operazione tentava di impostare i campi immagine. |
| `*`errorCount`*` | `xsd:int` | Sì | Il numero di errori generati quando l&#39;operazione tentava di impostare i campi immagine. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione tentava di applicare gli aggiornamenti. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano errori quando l’operazione tentava di applicare gli aggiornamenti. |

## Esempi {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Questo esempio imposta i dati nei campi di due immagini in una matrice di aggiornamento. Nella matrice, le immagini sono specificate dalle relative maniglie della risorsa e contengono la risoluzione in pixel, le coordinate di ancoraggio per posizione x e y e i dati utente. La risposta indica che i campi per entrambe le immagini sono stati impostati correttamente.

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
