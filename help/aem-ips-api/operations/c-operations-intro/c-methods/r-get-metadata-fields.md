---
description: Ottiene i campi di metadati definiti dall'utente associati a una risorsa.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic, SDK/API, Metadati
role: Developer,Administrator
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---

# getMetadataFields{#getmetadatafields}

Ottiene i campi di metadati definiti dall&#39;utente associati a una risorsa.

Sintassi

## Tipi di utenti autorizzati {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-bac949e59c0546429c5786fe422d750d}

**Input (getMetadataFieldsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;azienda gestisce. |
| `*`assetType`*` | `xsd:string` | Sì | Tipi di risorse da cui ottenere i metadati. |

**Output (getMetadataFieldsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`Frase di codice`*` | `Code Phrase` |  |  |

## Esempi {#section-dbfde1483d614b5aac2b491cb32115d7}

Questo esempio di codice restituisce le risorse di metadati per il tipo e la società specificati. La risposta contiene un array di campi di metadati in una matrice di campi. Non tutte le risorse hanno gli stessi metadati. L’utente IPS definisce il campo metadati della risorsa.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Risposta**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```
