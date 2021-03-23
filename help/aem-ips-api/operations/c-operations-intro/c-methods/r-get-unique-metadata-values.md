---
description: Ottiene valori di campo di metadati univoci.
seo-description: Ottiene valori di campo di metadati univoci.
seo-title: getUniqueMetadataValues
solution: Experience Manager
title: getUniqueMetadataValues
uuid: 5b2f95a7-cc0b-4938-99b9-2aefa0ffe693
feature: Dynamic Media Classic, SDK/API, Metadati
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 19%

---


# getUniqueMetadataValues{#getuniquemetadatavalues}

Ottiene valori di campo di metadati univoci.

Sintassi

## Tipi di utenti autorizzati {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-b9d1413811c24566b6d095701f0f66db}

**Input (getUniqueMetadataValuesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`fieldHandle`*` | `xsd:string` | No | Gestisci il campo dei metadati. |

**Output (getUniqueMetadataValuesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`values`*` | `type:StringArray` |  |  |

## Esempi {#section-440f3bc3e5be436cb6ec26117d05f476}

Questo esempio di codice utilizza un handle di campo per restituire valori di metadati specifici.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Risposta**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```

