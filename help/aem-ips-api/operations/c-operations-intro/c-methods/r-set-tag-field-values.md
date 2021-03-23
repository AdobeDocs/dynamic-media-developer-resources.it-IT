---
description: Imposta i valori del dizionario tag per un campo tag esistente.
seo-description: Imposta i valori del dizionario tag per un campo tag esistente.
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

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
