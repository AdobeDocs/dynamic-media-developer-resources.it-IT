---
description: Restituisce un array di nomi di percorsi di Photoshop per l'immagine specificata.
seo-description: Restituisce un array di nomi di percorsi di Photoshop per l'immagine specificata.
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
topic: Scene7 Image Production System API
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPhotoshopPathNames{#getphotoshoppathnames}

Restituisce un array di nomi di percorsi di Photoshop per l&#39;immagine specificata.

Sintassi

## Tipi di utenti autorizzati {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-605a4aab23104489a21f7f7f5849801b}

**Input (getPhotoshopPathNamesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Gestite la società che contiene l’immagine con cui desiderate lavorare. |
| ` *`assetHandle`*` | `xsd:string` | Sì | Consente di passare alla risorsa immagine. |

**Output (getPhotoshopPathNamesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`pathNameArray`*` | `types:StringArray` | Sì | Un array di nomi di percorsi Photoshop in un’immagine. |

## Esempi {#section-6d316f14b4184d42af4ca3f717b042dd}

**Request Contents (Richiesta contenuto)**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**Risposta**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

