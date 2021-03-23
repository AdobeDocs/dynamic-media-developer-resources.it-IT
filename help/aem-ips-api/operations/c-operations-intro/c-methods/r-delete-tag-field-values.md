---
description: Rimuove i valori dei campi tag dal dizionario di un campo tag.
seo-description: Rimuove i valori dei campi tag dal dizionario di un campo tag.
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 10%

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
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società contenente il campo tag. |
| `*`fieldHandle`*` | `xsd:string` | Sì | L’handle del campo tag da modificare. |
| `*`valueArray`*` | `types:StringArray` | Sì | Matrice di valori di tag da eliminare dal dizionario del campo. |

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
