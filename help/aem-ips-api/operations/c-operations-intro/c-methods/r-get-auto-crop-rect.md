---
description: Restituisce una regione ritagliata per un'immagine in base al colore di sfondo o alla trasparenza.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 10%

---

# getAutoCropRect{#getautocroprect}

Restituisce una regione ritagliata per un&#39;immagine in base al colore di sfondo o alla trasparenza.

Sintassi

## Tipi di utenti autorizzati {#section-32dfe7bb68764b93ae01e05ff7a7bdd0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-965d5973b8344d43a74b3e07cf0b7eb3}

**Input (getAutoCropRectParam)**

>[!NOTE]
>
>Specificare autoColorCropOptions o autoTransparentCropOptions quando si chiama questo metodo.

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle per l’azienda con la risorsa con cui desideri lavorare. |
| assetHandle | `xsd:string` | Sì | Handle della risorsa con cui desideri lavorare. |
| autoColorCropOptions | `types:AutoColorCropOptions` | No | Calcola il rettangolo di ritaglio in base al colore. Vedi [OpzioniRitaglioAutomatico](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| autoTransparentCropOptions | `types:AutoTransparentCropOptions` | No | Calcola il rettangolo di ritaglio in base alla trasparenza. Vedere [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Output (getAutoCropRectReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| xOffset | `xsd:int` | Sì | Coordinata iniziale in pixel a sinistra dell&#39;area di ritaglio calcolata. |
| Scostamento | `xsd:int` | Sì | Coordinata iniziale in pixel superiori dell&#39;area di ritaglio calcolata. |
| larghezza | `xsd:int` | Sì | Larghezza dell’area di ritaglio calcolata (in pixel). |
| altezza | `xsd:int` | Sì | Altezza dell’area di ritaglio calcolata (in pixel). |

## Esempi {#section-ba65bd66086d491cad1cea535954ee1f}

**Richiesta**

```java
<getAutoCropRectParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <companyHandle>c|3578</companyHandle>
  <assetHandle>a|3192146</assetHandle>
  <autoColorCropOptions>
    <corner>UpperLeft</corner>
    <tolerance>0.5</tolerance>
  </autoColorCropOptions>
</getAutoCropRectParam>
```

**Risposta**

```java
<getAutoCropRectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31-beta">
  <xOffset>452</xOffset>
  <yOffset>66</yOffset>
  <width>1271</width>
  <height>1874</height>
</getAutoCropRectReturn>
```

>[!MORELIKETHIS]
>
>* [OpzioniRitaglioAutomatico](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [OpzioniRitaglioTrasparenteAutomatico](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)
