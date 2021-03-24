---
description: Restituisce una matrice di nomi di percorso Photoshop per l'immagine specificata.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 16%

---


# getPhotoshopPathNames{#getphotoshoppathnames}

Restituisce una matrice di nomi di percorso Photoshop per l&#39;immagine specificata.

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
| `*`companyHandle`*` | `xsd:string` | Sì | Gestisci l&#39;azienda che contiene l&#39;immagine con cui desideri lavorare. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestisci la risorsa immagine. |

**Output (getPhotoshopPathNamesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | Sì | Matrice di nomi di percorsi Photoshop in un&#39;immagine. |

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

