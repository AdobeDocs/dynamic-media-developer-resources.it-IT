---
description: Elimina il campo di metadati di una società.
seo-description: Elimina il campo di metadati di una società.
seo-title: deleteMetadataField
solution: Experience Manager
title: deleteMetadataField
topic: Scene7 Image Production System API
uuid: 06ec434a-2793-4227-ac93-ae3871c38ab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# deleteMetadataField{#deletemetadatafield}

Elimina il campo di metadati di una società.

Sintassi

## Tipi di utenti autorizzati {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-73f12a30cc4340b6b32dd11effd5195e}

**Input (deleteMetadataFieldParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | handle della società che contiene il campo di metadati da eliminare. |
| ` *`fieldHandle`*` | `xsd:string` | Sì | handle del campo di metadati da eliminare. |

**Output (deleteMetadataFieldParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Questo esempio di codice elimina il campo di metadati di una società. Utilizza l&#39;handle della società e la gestione dei metadati come campi nel `deleteMetadataFieldParam` passato al server dei servizi Web IPS per eseguire questa azione.

**Request Contents (Richiesta contenuto)**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Risposta**

None.0
