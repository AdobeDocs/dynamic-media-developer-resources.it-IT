---
description: Elemento pattern con espressione regolare. Facoltativo negli elementi <rule>.
seo-description: Elemento pattern con espressione regolare. Facoltativo negli elementi <rule>.
seo-title: expression
solution: Experience Manager
title: expression
topic: Scene7 Image Serving - Image Rendering API
uuid: e7ef3769-0090-42d6-8021-1c213f1ee391
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# espressione{#expression}

Elemento pattern con espressione regolare. Facoltativo negli elementi `<rule>`.

## Attributi {#section-fd0574eee1f9423cbb2ed709c0906800}

Nessuno.

## Dati {#section-4cd740c511a1432da0955e9acfbcf96f}

Stringa di pattern con espressione regolare.

## Descrizione {#section-3245c8a531bb455d8398449f6ea63b37}

L&#39;elemento `<expression>` può essere vuoto o contenere una semplice stringa di ricerca o un pattern di espressione regolare. Il pattern viene applicato all&#39;intera stringa di richiesta.

Una corrispondenza si verifica sempre quando `<expression>` è vuoto o non è specificato; equivale a specificare `<expression>.*</expression>`.

L&#39;implementazione è basata sul pacchetto Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), che fornisce una sintassi con espressione regolare simile a quella di Perl.

## Nota {#section-6b41a900b0ce4a9590e5861e3c81599c}

La stringa di espressione non deve contenere caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<`, oppure l&#39;intera stringa può essere racchiusa in una sezione XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Tutti i caratteri compresi tra i tag `<expression>` e `</expression>` vengono passati al parser di espressioni regolari, inclusi i caratteri al di fuori della sezione opzionale `CDATA`. Fare attenzione a evitare spazi bianchi aggiuntivi.

## Consultate anche {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
