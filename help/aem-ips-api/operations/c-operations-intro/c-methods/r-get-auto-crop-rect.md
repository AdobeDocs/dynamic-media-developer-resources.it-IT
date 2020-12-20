---
description: Restituisce un’area ritagliata per un’immagine in base al colore di sfondo o alla trasparenza.
seo-description: Restituisce un’area ritagliata per un’immagine in base al colore di sfondo o alla trasparenza.
seo-title: getAutoCropRect
solution: Experience Manager
title: getAutoCropRect
topic: Scene7 Image Production System API
uuid: bb00d89a-5fc4-476f-aa47-3cf69ef99afe
translation-type: tm+mt
source-git-commit: 22b447e66c223126f4e6b91f9a0102e86731c4a4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# getAutoCropRect{#getautocroprect}

Restituisce un’area ritagliata per un’immagine in base al colore di sfondo o alla trasparenza.

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
>Quando si chiama questo metodo, specificare ` *`autoColorCropOptions`*` o ` *`autoTransparentCropOptions`*`.

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con la risorsa con cui desiderate lavorare. |
| ` *`assetHandle`*` | `xsd:string` | Sì | L’handle della risorsa con cui desiderate lavorare. |
| ` *`autoColorCropOptions`*` | `types:AutoColorCropOptions` | No | Calcola il rettangolo di ritaglio in base al colore. Vedere [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6). |
| ` *`autoTransparentCropOptions`*` | `types:AutoTransparentCropOptions` | No | Calcola il rettangolo di ritaglio in base alla trasparenza. Vedere [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b). |

**Output (getAutoCropRectReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`xOffset`*` | `xsd:int` | Sì | La coordinata dei pixel sinistro iniziali dell’area di ritaglio calcolata. |
| ` *`yOffset`*` | `xsd:int` | Sì | La coordinata del pixel superiore iniziale dell’area di ritaglio calcolata. |
| ` *`width`*` | `xsd:int` | Sì | Larghezza dell’area di ritaglio calcolata (in pixel). |
| ` *`height`*` | `xsd:int` | Sì | Altezza dell’area di ritaglio calcolata (in pixel). |

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
>* [AutoColorCropOptions](../../../types/c-data-types/r-auto-color-crop-options.md#reference-976c3a1f8e47473cae016a4e9e09e4a6)
>* [AutoTransparentCropOptions](../../../types/c-data-types/r-auto-transparent-crop-options.md#reference-f4460b3bdf814f4c85e4f097ea4e6e2b)

