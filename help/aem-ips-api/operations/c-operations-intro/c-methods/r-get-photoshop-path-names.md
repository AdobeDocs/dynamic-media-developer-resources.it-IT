---
description: Restituisce una matrice di nomi di percorso Photoshop per l'immagine specificata.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
TQID: 'https://experienceleague.adobe.com/BxFBNXpa9ilc4lXeXiuuvCQb9ChImZWt13-pJ3b3osk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 14%

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
| companyHandle | `xsd:string` | Sì | Gestisci fino all’azienda che contiene l’immagine con cui desideri lavorare. |
| assetHandle | `xsd:string` | Sì | Gestisci la risorsa immagine. |

**Output (getPhotoshopPathNamesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| pathNameArray | `types:StringArray` | Sì | Matrice di nomi di percorso Photoshop in un&#39;immagine. |

## Esempi {#section-6d316f14b4184d42af4ca3f717b042dd}

**Richiesta**

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
