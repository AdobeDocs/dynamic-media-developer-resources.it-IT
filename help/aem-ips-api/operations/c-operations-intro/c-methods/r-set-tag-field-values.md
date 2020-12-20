---
description: Imposta i valori dei dizionari di tag per un campo di tag esistente.
seo-description: Imposta i valori dei dizionari di tag per un campo di tag esistente.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Scene7 Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 12%

---


# setTagFieldValues{#settagfieldvalues}

Imposta i valori dei dizionari di tag per un campo di tag esistente.

Sintassi

## Tipi di utenti autorizzati {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-a05cbee4cb4f44198c414a6b14e69156}

**Ingresso**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`fieldHandle`*` | `xsd:string` | Sì | handle del campo del tag. |
| ` *`valueArray`*` | `types:StringArray` | Sì | Un array di valori di tag che sostituiscono il dizionario esistente del campo. Le associazioni di risorse vengono mantenute quando un nuovo valore corrisponde a un valore esistente. |

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
