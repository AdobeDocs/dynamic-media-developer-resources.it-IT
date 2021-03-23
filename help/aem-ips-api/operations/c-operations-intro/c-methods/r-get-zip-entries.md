---
description: Restituisce i dati del file ZIP.
seo-description: Restituisce i dati del file ZIP.
seo-title: getZipEntries
solution: Experience Manager
title: getZipEntries
uuid: cfc45f83-1cf9-4c50-9aac-5a731e62a839
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 17%

---


# getZipEntries{#getzipentries}

Restituisce i dati del file ZIP.

Sintassi

## Tipi di utenti autorizzati {#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-aa3f498fe76d4a5f99c42d64520fadce}

**Input (getZipEntriesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda che contiene il file Zip. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestisci il file Zip. |

**Output (getZipEntriesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | Sì | Array di voci in un file Zip. |

## Esempi {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

Questo esempio di codice restituisce informazioni sul file ZIP, incluse le dimensioni compresse e non compresse.

**Request Contents (Richiesta contenuto)**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**Risposta**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

