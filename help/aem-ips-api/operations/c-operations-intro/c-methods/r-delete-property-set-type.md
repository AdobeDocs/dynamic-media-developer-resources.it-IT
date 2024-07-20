---
description: Elimina un tipo di insieme di proprietà e il relativo insieme di proprietà associato e le proprietà.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 5%

---

# deletePropertySetType{#deletepropertysettype}

Elimina un tipo di insieme di proprietà e il relativo insieme di proprietà associato e le proprietà.

Sintassi

## Tipi di utenti autorizzati {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input (deletePropertySetTypeParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| typeHandle | `xsd:string` | Sì | Handle del tipo di set di proprietà da eliminare. |

**Output (deletePropertySetTypeParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-85faa2e3411a4e23aa6489037f7ce078}

In questo esempio di codice viene utilizzato l&#39;handle del tipo come campo in `deletePropertySetTypeParam` inviato al server dei servizi Web IPS per eliminare il tipo del set di proprietà.

**Richiesta**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Risposta**

Nessuno.
