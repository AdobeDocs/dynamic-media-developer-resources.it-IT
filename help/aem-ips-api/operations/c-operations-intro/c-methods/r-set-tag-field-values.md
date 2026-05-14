---
description: Imposta i valori del dizionario di tag per un campo tag esistente.
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
TQID: 'https://experienceleague.adobe.com/--ArL0CPejqbpJX-G7Z8zdU97WVXXjGfWc74UmOWSV0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 8%

---

# setTagFieldValues{#settagfieldvalues}

Imposta i valori del dizionario di tag per un campo tag esistente.

Sintassi

## Tipi di utenti autorizzati {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-a05cbee4cb4f44198c414a6b14e69156}

**Input**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| fieldHandle | `xsd:string` | Sì | Handle campo tag. |
| valueArray | `types:StringArray` | Sì | Matrice di valori di tag che sostituiscono il dizionario esistente del campo. Le associazioni tra risorse vengono mantenute quando un nuovo valore corrisponde a un valore esistente. |

**Output (setTagFieldValuesReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-b11cafd9bed54ab5836c737cc075c918}

**Richiesta**

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
