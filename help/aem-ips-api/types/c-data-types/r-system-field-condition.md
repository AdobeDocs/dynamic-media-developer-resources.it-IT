---
description: Una condizione di ricerca del campo di sistema per l’operazione searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# SystemFieldCondition{#systemfieldcondition}

Una condizione di ricerca del campo di sistema per l’operazione searchAssets.

Per i confronti unari, passare esattamente un valore ( `boolVal`, `longVal`, `doubleVal` o `dateVal`) a seconda del tipo di campo di sistema. Per gli intervalli di ricerca, passa i parametri `min<Type>` e `max<Type>` e passa un valore `op` di `Between` o `NotBetween`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`field`*` | `xsd:string` | Scelta dei campi del sistema di ricerca risorse. |
| `*`op`*` | `xsd:string` | Scelta degli operatori di confronto delle stringhe. |
| `*`value`*` | `xsd:string` | Valore su cui eseguire il test. |
| `*`boolVal`*` | `xsd:boolean` | Valore di confronto booleano. |
| `*`longVal`*` | `xsd:long` | Valore di confronto lungo. |
| `*`minLong`*` | `xsd:long` | Limite inferiore di lungo intervallo. |
| `*`maxLong`*` | `xsd:long` | Limite superiore di un lungo intervallo. |
| `*`doubleVal`*` | `xsd:double` | Valore di confronto doppio. |
| `*`minDouble`*` | `xsd:double` | Limite inferiore della doppia gamma. |
| `*`maxDouble`*` | `xsd:double` | Limite superiore di doppio intervallo. |
| `*`dateVal`*` | `xsd:dateTime` | Valore di confronto delle date. |
| `*`minDate`*` | `xsd:dateTime` | Intervallo di date minimo. |
| `*`maxDate`*` | `xsd:dateTime` | Massimo intervallo di date. |

## Esempio {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```
