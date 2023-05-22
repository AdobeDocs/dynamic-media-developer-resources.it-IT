---
description: Elemento pattern con espressione regolare. Opzionale in <rule> elementi.
solution: Experience Manager
title: espressione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 3%

---

# espressione{#expression}

Elemento pattern con espressione regolare. Opzionale in `<rule>` elementi.

## Attributi {#section-fd0574eee1f9423cbb2ed709c0906800}

Nessuno.

## Dati {#section-4cd740c511a1432da0955e9acfbcf96f}

Stringa di pattern con espressione regolare.

## Descrizione {#section-3245c8a531bb455d8398449f6ea63b37}

Il `<expression>` L&#39;elemento può essere vuoto o contenere una stringa di ricerca semplice o un pattern di espressione regolare. Il pattern viene applicato all’intera stringa di richiesta.

Una corrispondenza si verifica sempre quando `<expression>` è vuoto o non specificato; equivale a specificare `<expression>.*</expression>`.

L’implementazione si basa sul pacchetto Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), che fornisce una sintassi per espressioni regolari simile a quella di Perl.

## Nota {#section-6b41a900b0ce4a9590e5861e3c81599c}

La stringa di espressione non deve contenere i caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati con `&` e `<`, rispettivamente, o l&#39;intera stringa può essere racchiusa in un XML `CDATA` sezione:

`<expression><![CDATA[&fmt=custom]]></expression>`

Tutti i caratteri compresi tra `<expression>` e `</expression>` I tag vengono passati al parser di espressioni regolari, inclusi i caratteri al di fuori del `CDATA` sezione. Prestare attenzione per evitare spazi vuoti aggiuntivi.

## Consultate anche {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
