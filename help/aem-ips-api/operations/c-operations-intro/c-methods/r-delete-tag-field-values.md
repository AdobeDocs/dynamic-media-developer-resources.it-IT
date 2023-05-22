---
description: Rimuove i valori dei campi tag dal dizionario di un campo tag.
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 11%

---

# deleteTagFieldValues{#deletetagfieldvalues}

Rimuove i valori dei campi tag dal dizionario di un campo tag.

## Tipi di utenti autorizzati {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-5db64a6ae238426395bc760b83587260}

**Input (deleteTagFieldValuesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle della società contenente il campo tag. |
| fieldHandle | `xsd:string` | Sì | Handle del campo tag da modificare. |
| valueArray | `types:StringArray` | Sì | Matrice di valori tag da eliminare dal dizionario del campo. |

**Output (deleteTagFieldValuesParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-92f9e575a6da491caa09e264b4d6ee55}

**Request Contents (Richiesta contenuto)**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**Risposta**

Nessuno.
