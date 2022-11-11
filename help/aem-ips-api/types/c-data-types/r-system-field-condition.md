---
description: Una condizione di ricerca del campo di sistema per l’operazione searchAssets.
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 5%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Una condizione di ricerca del campo di sistema per l’operazione searchAssets.

Per i confronti unari, passa esattamente un valore ( `boolVal`, `longVal`, `doubleVal`oppure `dateVal`) a seconda del tipo di campo di sistema. Per gli intervalli di ricerca, passa `min<Type>` e `max<Type>` e trasmettere un `op` valore `Between` o `NotBetween`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| field | `xsd:string` | Scelta dei campi del sistema di ricerca risorse. |
| op | `xsd:string` | Scelta degli operatori di confronto delle stringhe. |
| value | `xsd:string` | Valore su cui eseguire il test. |
| boolVal | `xsd:boolean` | Valore di confronto booleano. |
| longVal | `xsd:long` | Valore di confronto lungo. |
| minLong | `xsd:long` | Limite inferiore di lungo intervallo. |
| maxLong | `xsd:long` | Limite superiore di un lungo intervallo. |
| doubleVal | `xsd:double` | Valore di confronto doppio. |
| minDouble | `xsd:double` | Limite inferiore della doppia gamma. |
| maxDouble | `xsd:double` | Limite superiore di doppio intervallo. |
| dateVal | `xsd:dateTime` | Valore di confronto delle date. |
| minDate | `xsd:dateTime` | Intervallo di date minimo. |
| maxDate | `xsd:dateTime` | Massimo intervallo di date. |

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
