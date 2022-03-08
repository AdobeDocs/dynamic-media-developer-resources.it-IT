---
description: Aggiunge nuovi valori tag al dizionario di un campo tag esistente.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 12%

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
| companyHandle | `xsd:string` | Sì | L&#39;handle della società contenente il campo tag. |
| fieldHandle | `xsd:string` | Sì | L’handle del campo tag da modificare. |
| valueArray | `xsd:string` | Sì | Matrice di valori tag da aggiungere al dizionario esistente del campo. |

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
