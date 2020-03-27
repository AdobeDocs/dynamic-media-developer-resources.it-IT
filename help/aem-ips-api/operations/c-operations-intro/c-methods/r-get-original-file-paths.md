---
description: Ottiene i percorsi di file originali delle risorse di una società.
seo-description: Ottiene i percorsi di file originali delle risorse di una società.
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
topic: Scene7 Image Production System API
uuid: c4acf288-1a57-4295-806b-348f15a089cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Sì | Array di handle per risorse il cui percorso file originale si desidera ottenere. |

**Output (getOriginalFilePathsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`OriginalFileArray`*` | `types:StringArray` | Sì | Matrice di stringhe che rappresentano i percorsi di file originali. |

## Esempi {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Questo esempio di codice restituisce i percorsi dei file delle risorse specificati con le maniglie delle risorse univoche in un array di handle della risorsa.

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

