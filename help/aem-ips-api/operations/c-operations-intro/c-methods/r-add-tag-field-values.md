---
description: Aggiunge nuovi valori tag al dizionario di un campo tag esistente.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 11%

---


# addTagFieldValues{#addtagfieldvalues}

Aggiunge nuovi valori tag al dizionario di un campo tag esistente.

Sintassi

## Tipi di utenti autorizzati {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società contenente il campo tag. |
| `*`fieldHandle`*` | `xsd:string` | Sì | L’handle del campo tag da modificare. |
| `*`valueArray`*` | `xsd:string` | Sì | Matrice di valori tag da aggiungere al dizionario esistente del campo. |

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
