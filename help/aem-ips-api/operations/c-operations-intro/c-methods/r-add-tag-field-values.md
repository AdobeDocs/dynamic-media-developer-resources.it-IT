---
description: Aggiunge nuovi valori di tag al dizionario di un campo tag esistente.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
TQID: 'https://experienceleague.adobe.com/-DA9IYswE5Mfflys-Cn0Gi62OsMU3O1QYIIKYJNq9QU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 7%

---

# addTagFieldValues{#addtagfieldvalues}

Aggiunge nuovi valori di tag al dizionario di un campo tag esistente.

Sintassi

## Tipi di utenti autorizzati {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle della società contenente il campo tag. |
| fieldHandle | `xsd:string` | Sì | Handle del campo tag da modificare. |
| valueArray | `xsd:string` | Sì | Matrice di valori di tag da aggiungere al dizionario esistente del campo. |

**Output (addTagFieldValuesParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-c4049392f1c548f883b8b1f8f167bada}

**Richiesta**

```java {.line-numbers}
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
