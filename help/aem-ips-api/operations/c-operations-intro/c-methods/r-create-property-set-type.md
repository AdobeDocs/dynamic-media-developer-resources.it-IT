---
description: Un tipo di set di proprietà specifica le varie impostazioni utilizzate per gestire i set di proprietà.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 10%

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
