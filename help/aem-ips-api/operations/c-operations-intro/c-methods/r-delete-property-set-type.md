---
description: Elimina un tipo di set di proprietà e le relative proprietà e set di proprietà associate.
seo-description: Elimina un tipo di set di proprietà e le relative proprietà e set di proprietà associate.
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
topic: Scene7 Image Production System API
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 8%

---


# deletePropertySetType{#deletepropertysettype}

Elimina un tipo di set di proprietà e le relative proprietà e set di proprietà associate.

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
| ` *`typeHandle`*` | `xsd:string` | Sì | L&#39;handle del tipo di set di proprietà da eliminare. |

**Output (deletePropertySetTypeParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-85faa2e3411a4e23aa6489037f7ce078}

Questo esempio di codice utilizza l&#39;handle del tipo come campo nel `deletePropertySetTypeParam` inviato al server dei servizi Web IPS per eliminare il tipo di set di proprietà.

**Request Contents (Richiesta contenuto)**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Risposta**

Nessuno.
