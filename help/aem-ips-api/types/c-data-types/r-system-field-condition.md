---
description: Una condizione di ricerca del campo di sistema per l'operazione searchAssets.
seo-description: Una condizione di ricerca del campo di sistema per l'operazione searchAssets.
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
topic: Scene7 Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SystemFieldCondition{#systemfieldcondition}

Una condizione di ricerca del campo di sistema per l&#39;operazione searchAssets.

Per i confronti unari, trasmettere esattamente un valore ( `boolVal`, `longVal`, `doubleVal`o `dateVal`) a seconda del tipo di campo di sistema. Per gli intervalli di ricerca, passate `min<Type>` e `max<Type>` i parametri e passate un `op` valore di `Between` o `NotBetween`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`field`*` | `xsd:string` | Scelta dei campi del sistema di ricerca risorse. |
| ` *`op`*` | `xsd:string` | Scelta degli operatori di confronto delle stringhe. |
| ` *`value`*` | `xsd:string` | Valore su cui eseguire il test. |
| ` *`boolVal`*` | `xsd:boolean` | Valore di confronto booleano. |
| ` *`longVal`*` | `xsd:long` | Valore di confronto lungo. |
| ` *`minLong`*` | `xsd:long` | Limite inferiore dell&#39;intervallo lungo. |
| ` *`maxLong`*` | `xsd:long` | Limite superiore dell&#39;intervallo lungo. |
| ` *`doubleVal`*` | `xsd:double` | Valore di confronto doppio. |
| ` *`minDouble`*` | `xsd:double` | Limite inferiore del doppio intervallo. |
| ` *`maxDouble`*` | `xsd:double` | Limite superiore del doppio intervallo. |
| ` *`dateVal`*` | `xsd:dateTime` | Valore di confronto delle date. |
| ` *`minDate`*` | `xsd:dateTime` | Intervallo di date minimo. |
| ` *`maxDate`*` | `xsd:dateTime` | Massimo intervallo di date. |

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

