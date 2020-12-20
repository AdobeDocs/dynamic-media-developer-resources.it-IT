---
description: Elemento stringa di sostituzione. Facoltativo negli elementi <rule>.
seo-description: Elemento stringa di sostituzione. Facoltativo negli elementi <rule>.
seo-title: replace
solution: Experience Manager
title: replace
topic: Scene7 Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# replace{#substitution}

Elemento stringa di sostituzione. Facoltativo negli elementi `<rule>`.

## Attributi {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Nessuno.

## Dati {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Stringa di sostituzione.

## Descrizione {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definisce una stringa sostitutiva per la stringa o sottostringa associata nel percorso o nella query.

Se l&#39;espressione del pattern include sottoespressioni (delimitate da parentesi), la prima sottostringa corrispondente viene sostituita con la stringa di sostituzione. Se l&#39;espressione del pattern non include sottoespressioni, viene sostituita l&#39;intera stringa corrispondente.

Se `<expression>` è vuoto o assente, la stringa di sostituzione viene aggiunta al percorso o alla query.

Se `<substitution>` è vuoto, la stringa o la sottostringa corrispondente viene rimossa. Se `<substitution>` non è specificato, il percorso o la stringa di query non viene modificata.

>[!NOTE]
>
>Tutte le corrispondenze nella stringa di input vengono sostituite quando `replace="all"` viene specificato nell&#39; `<rule>`,elemento a cui appartiene l&#39;elemento `<substitution>`. Per impostazione predefinita, solo la prima corrispondenza viene sostituita con la stringa di sostituzione.

## Nota {#section-cedf2adabaaf441c9f598fb0ea180246}

La stringa di sostituzione non deve contenere caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<`, oppure l&#39;intera stringa può essere racchiusa in una sezione CDATA XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
