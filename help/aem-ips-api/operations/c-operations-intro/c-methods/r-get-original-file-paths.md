---
description: Ottiene i percorsi file originali delle risorse di un’azienda.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 13%

---

# getOriginalFilePaths{#getoriginalfilepaths}

Ottiene i percorsi file originali delle risorse di un’azienda.

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
| companyHandle | `xsd:string` | Sì | La maniglia per l&#39;azienda. |
| assetHandleArray | `types:HandleArray` | Sì | Array di handle per le risorse di cui desideri ottenere il percorso file originale. |

**Output (getOriginalFilePathsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| originalFileArray | `types:StringArray` | Sì | Matrice di stringhe che rappresentano i percorsi dei file originali. |

## Esempi {#section-a966e783a2ba49f5b6b0f961329ab2f8}

In questo esempio di codice vengono restituiti i percorsi file delle risorse specificate con handle di risorse univoci in un array di handle di risorse.

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
