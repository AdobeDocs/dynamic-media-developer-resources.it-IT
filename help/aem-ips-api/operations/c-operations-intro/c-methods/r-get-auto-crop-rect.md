---
description: Restituisce un'area ritagliata per un'immagine in base al colore di sfondo o alla trasparenza.
solution: Experience Manager
title: getAutoCropRect
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: e291597a-b863-42dd-88dc-13398b734410
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 13%

---

# getAutoCropRect{#getautocroprect}

Restituisce un&#39;area ritagliata per un&#39;immagine in base al colore di sfondo o alla trasparenza.

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
>Quando si chiama questo metodo, specificare `*`autoColorCropOptions`*` o `*`autoTransparentCropOptions`*`.

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda con la risorsa con cui desideri lavorare. |
| `*`assetHandle`*` | `xsd:string` | Sì | Il handle della risorsa con cui desideri lavorare. |
| `*`autoColorCropOptions`*` | `types:AutoColorCropOptions` | No | Calcola il rettangolo di ritaglio in base al colore. Vedere [Opzioni di ritaglio automatico](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| `*`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | No | Calcola il rettangolo di ritaglio in base alla trasparenza. Vedere [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Output (getAutoCropRectReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`xOffset`*` | `xsd:int` | Sì | Coordinata dei pixel sinistro iniziali dell&#39;area di ritaglio calcolata. |
| `*`yOffset`*` | `xsd:int` | Sì | La coordinata del pixel superiore iniziale dell&#39;area di ritaglio calcolata. |
| `*`width`*` | `xsd:int` | Sì | Larghezza dell’area di ritaglio calcolata (in pixel). |
| `*`height`*` | `xsd:int` | Sì | Altezza dell’area di ritaglio calcolata (in pixel). |

## Esempi {#section-ba65bd66086d491cad1cea535954ee1f}

**Request Contents (Richiesta contenuto)**

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
>* [OpzioniRitaglioColoreAutomatico](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
* [OpzioniRitaglioAutomaticoTrasparente](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

