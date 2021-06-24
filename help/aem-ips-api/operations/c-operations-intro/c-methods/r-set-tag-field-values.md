---
description: Imposta i valori del dizionario tag per un campo tag esistente.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 12%

---

# setTagFieldValues{#settagfieldvalues}

Imposta i valori del dizionario tag per un campo tag esistente.

Sintassi

## Tipi di utenti autorizzati {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-a05cbee4cb4f44198c414a6b14e69156}

**Ingresso**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`fieldHandle`*` | `xsd:string` | Sì | Maniglia del campo di tag. |
| `*`valueArray`*` | `types:StringArray` | Sì | Matrice di valori tag che sostituiscono il dizionario esistente del campo. Le associazioni delle risorse vengono mantenute quando un nuovo valore corrisponde a un valore esistente. |

**Output (setTagFieldValuesReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-b11cafd9bed54ab5836c737cc075c918}

**Request Contents (Richiesta contenuto)**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**Risposta**

Nessuno.
