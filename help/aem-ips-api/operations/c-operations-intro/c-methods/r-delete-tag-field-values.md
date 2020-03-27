---
description: Rimuove i valori dei campi tag dal dizionario di un campo di tag.
seo-description: Rimuove i valori dei campi tag dal dizionario di un campo di tag.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Scene7 Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
translation-type: tm+mt
source-git-commit: b5eaefb375fbd0d0786619fa6d84b4f6fc17a77f

---


# deleteTagFieldValues{#deletetagfieldvalues}

Rimuove i valori dei campi tag dal dizionario di un campo di tag.

## Tipi di utenti autorizzati {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-5db64a6ae238426395bc760b83587260}

**Input (deleteTagFieldValuesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società che contiene il campo del tag. |
| ` *`fieldHandle`*` | `xsd:string` | Sì | handle del campo tag da modificare. |
| ` *`valueArray`*` | `types:StringArray` | Sì | Un array di valori di tag da eliminare dal dizionario del campo. |

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
