---
description: Verifica la presenza di conflitti di ID IPS confrontando i nomi delle risorse con tutti i nomi dello spazio dei nomi del catalogo Image Server/Image Rendering di un’azienda.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
TQID: 'https://experienceleague.adobe.com/RbFXhRqcaGXLMAeJhXMzho-ylSe2ktcKwvdbFtrcppM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 9%

---

# checkAssetNames{#checkassetnames}

Verifica la presenza di conflitti di ID IPS confrontando i nomi delle risorse con tutti i nomi dello spazio dei nomi del catalogo Image Server/Image Rendering di un’azienda.

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
| companyHandle | `xsd:string` | No | Handle per l&#39;azienda che contiene l&#39;utente. |
| assetNamesArray | `types:StringArray` | Sì | Matrice di nomi di risorse da verificare. |

**Output (checkAssetNamesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | Sì | Matrice di nomi di risorse in uso. |

## Esempi {#section-bc5d120d74614a63a425ca3acc337219}

Questo codice di esempio richiede i nomi delle risorse in uso per una società specificata. La risposta restituisce una matrice di nomi di risorse in uso.

**Richiesta**

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
