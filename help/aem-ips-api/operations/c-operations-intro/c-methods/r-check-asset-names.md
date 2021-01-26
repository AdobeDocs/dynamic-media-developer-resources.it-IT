---
description: Controlla i conflitti degli ID IPS confrontando i nomi delle risorse con tutti i nomi dello spazio dei nomi del catalogo Image Serving/Image Rendering di una società.
seo-description: Controlla i conflitti degli ID IPS confrontando i nomi delle risorse con tutti i nomi dello spazio dei nomi del catalogo Image Serving/Image Rendering di una società.
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Dynamic Media Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 9%

---


# checkAssetNames{#checkassetnames}

Controlla i conflitti degli ID IPS confrontando i nomi delle risorse con tutti i nomi dello spazio dei nomi del catalogo Image Serving/Image Rendering di una società.

Sintassi

## Tipi di utenti autorizzati {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parametri {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Input (checkAssetNamesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | No | L’handle della società che contiene l’utente. |
| `*`assetNamesArray`*` | `types:StringArray` | Sì | Un array di nomi di risorse da controllare. |

**Output (checkAssetNamesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`inUseNameArray`*` | `types:StringArray` | Sì | Un array di nomi di risorse in uso. |

## Esempi {#section-bc5d120d74614a63a425ca3acc337219}

Questo codice di esempio richiede i nomi delle risorse in uso per una società specificata. La risposta restituisce un array di nomi di risorse in uso.

**Request Contents (Richiesta contenuto)**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Risposta**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```

