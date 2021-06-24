---
description: Restituisce le coordinate del quadrilatero che racchiude il percorso Photoshop denominato.
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 16%

---

# getPhotoshopPath{#getphotoshoppath}

Restituisce le coordinate del quadrilatero che racchiude il percorso Photoshop denominato.

Sintassi

## Tipi di utenti autorizzati {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parametri {#section-ebffe496284c4ced9f329f78127be199}

**Input (getPhotoshopPathParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Gestisci l&#39;azienda con l&#39;immagine con cui vuoi lavorare. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestisci la risorsa immagine. |
| `*`pathName`*` | `xsd:string` | Sì | Nome del percorso Photoshop che si desidera restituire. |

**Output (getPhotoshopPathReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`prospettivaQuad`*` | `types:PerspectiveQuad` | Sì | Restituisce le coordinate immagine in base al percorso. Vedere [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204). |

## Esempi {#section-1f0461cbdc184c8d8925336d5279db47}

**Request Contents (Richiesta contenuto)**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**Risposta**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [PerspectiveQuad](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)

