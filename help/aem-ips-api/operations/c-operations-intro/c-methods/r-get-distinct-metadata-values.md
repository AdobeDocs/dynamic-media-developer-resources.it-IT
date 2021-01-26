---
description: Restituisce tutti i valori per un campo di metadati.
seo-description: Restituisce tutti i valori per un campo di metadati.
seo-title: getDistinctMetadataValues
solution: Experience Manager
title: getDistinctMetadataValues
topic: Dynamic Media Image Production System API
uuid: 47c1d3a3-9f33-4c36-828a-e858370997d1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 19%

---


# getDistinctMetadataValues{#getdistinctmetadatavalues}

Restituisce tutti i valori per un campo di metadati.

Sintassi

## Tipi di utenti autorizzati {#section-f0f44fdcb318490582dd04de8eaf745d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-600f36a32ff147cb83149943d37843e2}

**Input (getDistinctMetadataValuesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle della società per la quale si desidera ottenere i dati. |
| `*`metadataKey`*` | `xsd:string` | Sì | Chiave metadati nella notazione del punto. |

**Output (getDistinctMetadataValuesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`valueArray`*` | `types:ValueArray` | Sì | Valori del campo di metadati richiesto. |

## Esempi {#section-0189fa6fb31646cda5ce1b0bc4fcdf46}

**Request Contents (Richiesta contenuto)**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
         <xsd:user>user@company.com</xsd:user>
         <xsd:password>password</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
   <ns:getDistinctMetadataValuesParam>
      <ns:companyHandle>680</ns:companyHandle>
      <ns:metadataKey>dc.format</ns:metadataKey>
      </ns:getDistinctMetadataValuesParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**Risposta**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <getDistinctMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <valueArray>
            <items>
               <value>N/A</value>
               <count>412</count>
            </items>
            <items>
               <value>image/jpeg</value>
               <count>189</count>
            </items>
            <items>
               <value>image/epsf</value>
               <count>1</count>
            </items>
            <items>
               <value>image/tiff</value>
               <count>3</count>
            </items>
         </valueArray>
      </getDistinctMetadataValuesReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

