---
description: Ottiene i campi di metadati definiti dall'utente associati a una risorsa.
seo-description: Ottiene i campi di metadati definiti dall'utente associati a una risorsa.
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
feature: Dynamic Media Classic, SDK/API, Metadati
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 11%

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

