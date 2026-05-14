---
description: Un tipo di insieme di proprietà specifica varie impostazioni utilizzate per gestire gli insiemi di proprietà.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
TQID: 'https://experienceleague.adobe.com/JOAxK9j-P0v8inQRU65C2rVCM9-OnXTXCF6wtp6eksY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 8%

---

# createPropertySetType{#createpropertysettype}

Un tipo di insieme di proprietà specifica varie impostazioni utilizzate per gestire gli insiemi di proprietà.

Sintassi

## Tipi di utenti autorizzati {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-43dece72eb9f44df80f4a119dd2c008b}

**Input (createPropertySetTypeParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | No | Handle per l&#39;azienda a cui appartiene il tipo di set di proprietà. Se `companyHandle` non viene passato e il chiamante è un `IpsAdmin`, viene creato un tipo di set di proprietà globale. |
| nome | `xsd:string` | Sì | Nome del tipo di set di proprietà. |
| propertyType | `xsd:string` | Sì | Scelta dei tipi di set di proprietà. |
| allowMultiple | `xsd:boolean` | Sì | Determina se il programma può avere più insiemi di proprietà. |

**Output (createPropertySetTypeReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| typeHandle | `xsd:string` | Sì | Handle al tipo. |

## Esempi {#section-13396c9639a6475190e622eae3cdb534}

In questo esempio di codice viene creato un set di proprietà con un nome e un tipo specificati dalla costante `PropertySet Types`. Handle per l&#39;azienda a cui appartiene il tipo di set di proprietà. Se companyHandle non viene passato e il chiamante è un IpsAdmin, viene creato un tipo di insieme di proprietà globale.

**Richiesta**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**Risposta**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```
