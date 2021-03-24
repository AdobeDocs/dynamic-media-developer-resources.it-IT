---
description: Ottiene i percorsi di file originali delle risorse di una società.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 13%

---


# getOriginalFilePaths{#getoriginalfilepaths}

Ottiene i percorsi di file originali delle risorse di una società.

Sintassi

## Tipi di utenti autorizzati {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Richiede l’accesso in lettura alla risorsa.

## Parametri {#section-a6b394daba6e49a8882cf3051035d9d1}

**Input (getOriginalFilePathsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Il manico per l&#39;azienda. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sì | Array di handle alle risorse di cui si desidera ottenere il percorso file originale. |

**Output (getOriginalFilePathsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | Sì | Matrice di stringhe che rappresentano i percorsi file originali. |

## Esempi {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Questo esempio di codice restituisce i percorsi di file delle risorse specificate con handle di risorsa univoci in un array di handle di risorsa.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**Risposta**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

