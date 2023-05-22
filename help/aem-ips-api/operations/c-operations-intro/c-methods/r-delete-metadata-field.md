---
description: Elimina il campo di metadati di un’azienda.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 8%

---

# deleteMetadataField{#deletemetadatafield}

Elimina il campo di metadati di un’azienda.

Sintassi

## Tipi di utenti autorizzati {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-73f12a30cc4340b6b32dd11effd5195e}

**Input (deleteMetadataFieldParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda contenente il campo di metadati da eliminare. |
| fieldHandle | `xsd:string` | Sì | Handle del campo metadati da eliminare. |

**Output (deleteMetadataFieldParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Questo esempio di codice elimina il campo di metadati di un’azienda. Utilizza l’handle aziendale e l’handle dei metadati come campi nella sezione `deleteMetadataFieldParam` passato al server dei servizi Web IPS per eseguire questa azione.

**Request Contents (Richiesta contenuto)**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Risposta**

Nessuno.0
