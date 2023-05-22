---
description: Ottiene i campi di metadati definiti dall'utente associati a una risorsa.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
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
| companyHandle | `xsd:string` | Sì | La maniglia aziendale. |
| assetType | `xsd:string` | Sì | Tipi di risorse da cui ottenere i metadati. |

**Output (getMetadataFieldsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| Frase codice | `Code Phrase` |  |  |

## Esempi {#section-dbfde1483d614b5aac2b491cb32115d7}

In questo esempio di codice vengono restituite le risorse di metadati per il tipo e la società specificati. La risposta contiene un array di campi di metadati in un array di campi. Non tutte le risorse hanno gli stessi metadati. L’utente IPS definisce il campo di metadati della risorsa.

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
