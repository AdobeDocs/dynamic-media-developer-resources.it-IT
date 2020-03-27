---
description: Aggiunge nuovi valori di tag al dizionario di un campo di tag esistente.
seo-description: Aggiunge nuovi valori di tag al dizionario di un campo di tag esistente.
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: 9304f02c-a1df-4477-ab33-f2491c390c92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addTagFieldValues{#addtagfieldvalues}

Aggiunge nuovi valori di tag al dizionario di un campo di tag esistente.

Sintassi

## Tipi di utenti autorizzati {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società che contiene il campo del tag. |
| ` *`fieldHandle`*` | `xsd:string` | Sì | handle del campo tag da modificare. |
| ` *`valueArray`*` | `xsd:string` | Sì | Un array di valori di tag da aggiungere al dizionario esistente del campo. |

**Output (addTagFieldValuesParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-c4049392f1c548f883b8b1f8f167bada}

**Request Contents (Richiesta contenuto)**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Risposta**

Nessuno.
