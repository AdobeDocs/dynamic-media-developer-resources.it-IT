---
description: Condizione di ricerca del campo di sistema per l’operazione searchAssets.
solution: Experience Manager
title: CondizioneCampoSistema
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Condizione di ricerca del campo di sistema per l’operazione searchAssets.

Per confronti unari, trasmettere esattamente un valore ( `boolVal`, `longVal`, `doubleVal`, o `dateVal`) a seconda del tipo di campo di sistema. Per gli intervalli di ricerca, trasmettere `min<Type>` e `max<Type>` e trasmettere un `op` valore di `Between` o `NotBetween`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| campo | `xsd:string` | Scelta dei campi del sistema di ricerca delle risorse. |
| op | `xsd:string` | Scelta degli operatori di confronto delle stringhe. |
| valore | `xsd:string` | Valore su cui eseguire il test. |
| boolVal | `xsd:boolean` | Valore di confronto booleano. |
| longVal | `xsd:long` | Valore di confronto lungo. |
| minLong | `xsd:long` | Limite inferiore del lungo raggio. |
| maxLong | `xsd:long` | Limite superiore del lungo raggio. |
| doubleVal | `xsd:double` | Valore di confronto doppio. |
| minDouble | `xsd:double` | Limite inferiore dell&#39;intervallo doppio. |
| maxDouble | `xsd:double` | Limite superiore del doppio intervallo. |
| dateVal | `xsd:dateTime` | Valore di confronto delle date. |
| minDate | `xsd:dateTime` | Intervallo di date minimo. |
| maxDate | `xsd:dateTime` | Intervallo di date massimo. |

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
