---
description: Elemento pattern con espressione regolare. Facoltativo negli elementi <rule>.
solution: Experience Manager
title: espressione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
TQID: 'https://experienceleague.adobe.com/zMAFfzeypXmMIx1aO1xmHdF-UkHJPHKp7KUgi05F94w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 2%

---

# espressione{#expression}

Elemento pattern con espressione regolare. Facoltativo negli elementi `<rule>`.

## Attributi {#section-fd0574eee1f9423cbb2ed709c0906800}

Nessuno.

## Dati {#section-4cd740c511a1432da0955e9acfbcf96f}

Stringa di pattern con espressione regolare.

## Descrizione {#section-3245c8a531bb455d8398449f6ea63b37}

L&#39;elemento `<expression>` può essere vuoto o contenere una stringa di ricerca semplice o un pattern di espressione regolare. Il pattern viene applicato all’intera stringa di richiesta.

Una corrispondenza si verifica sempre quando `<expression>` è vuoto o non è specificato; ciò equivale a specificare `<expression>.*</expression>`.

L&#39;implementazione si basa sul pacchetto Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), che fornisce una sintassi per espressioni regolari simile a quella di Perl.

## Nota {#section-6b41a900b0ce4a9590e5861e3c81599c}

La stringa di espressione non deve contenere i caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<` oppure l&#39;intera stringa può essere racchiusa in una sezione XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Tutti i caratteri compresi tra i tag `<expression>` e `</expression>` vengono passati al parser di espressioni regolari, inclusi i caratteri all&#39;esterno della sezione facoltativa `CDATA`. Prestare attenzione per evitare spazi vuoti aggiuntivi.

## Consultate anche {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
