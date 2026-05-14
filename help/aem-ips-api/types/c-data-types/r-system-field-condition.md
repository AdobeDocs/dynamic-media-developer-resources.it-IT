---
description: Condizione di ricerca del campo di sistema per l’operazione searchAssets.
solution: Experience Manager
title: CondizioneCampoSistema
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

Condizione di ricerca del campo di sistema per l’operazione searchAssets.

Per confronti unari, passare esattamente un valore ( `boolVal`, `longVal`, `doubleVal` o `dateVal`) a seconda del tipo di campo di sistema. Per gli intervalli di ricerca, passare `min<Type>` e `max<Type>` parametri e un valore `op` di `Between` o `NotBetween`.

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
