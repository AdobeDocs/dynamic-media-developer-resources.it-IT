---
description: Un tipo di set di proprietà specifica le varie impostazioni utilizzate per gestire i set di proprietà.
seo-description: Un tipo di set di proprietà specifica le varie impostazioni utilizzate per gestire i set di proprietà.
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 9%

---


# createPropertySetType{#createpropertysettype}

Un tipo di set di proprietà specifica le varie impostazioni utilizzate per gestire i set di proprietà.

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
| `*`companyHandle`*` | `xsd:string` | No | L&#39;handle della società proprietaria del tipo di set di proprietà. Se `companyHandle` non viene passato e il chiamante è un `IpsAdmin`, verrà creato un tipo di set di proprietà globale. |
| `*`name`*` | `xsd:string` | Sì | Nome del tipo di set di proprietà. |
| `*`propertyType`*` | `xsd:string` | Sì | Scelta dei tipi di set di proprietà. |
| `*`allowMultiple`*` | `xsd:boolean` | Sì | Determina se il programma può avere più set di proprietà. |

**Output (createPropertySetTypeReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Sì | Un handle per il tipo. |

## Esempi {#section-13396c9639a6475190e622eae3cdb534}

Questo esempio di codice crea una proprietà impostata con un nome e un tipo specificati dalla costante `PropertySet Types`. L&#39;handle della società proprietaria del tipo di set di proprietà. Se companyHandle non viene passato e il chiamante è un IpsAdmin, verrà creato un tipo di set di proprietà globale.

**Request Contents (Richiesta contenuto)**

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

