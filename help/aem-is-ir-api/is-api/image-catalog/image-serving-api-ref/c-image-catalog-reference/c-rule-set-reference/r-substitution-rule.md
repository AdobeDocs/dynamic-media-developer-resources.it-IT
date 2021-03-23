---
description: Elemento della stringa di sostituzione. Facoltativo negli elementi <rule> .
seo-description: Elemento della stringa di sostituzione. Facoltativo negli elementi <rule> .
seo-title: sostituzione
solution: Experience Manager
title: sostituzione
uuid: e5730559-0512-4416-927d-a7faf9180741
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# substitution{#substitution}

Elemento della stringa di sostituzione. Facoltativo negli elementi `<rule>`.

## Attributi {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Nessuno.

## Dati {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Stringa di sostituzione.

## Descrizione {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definisce una stringa sostitutiva per la stringa o sottostringa corrispondente nel percorso o nella query.

Se l&#39;espressione del pattern include espressioni secondarie (delimitate da parentesi), la prima stringa secondaria corrispondente viene sostituita dalla stringa di sostituzione. Se l&#39;espressione del pattern non include sottoespressioni, viene sostituita l&#39;intera stringa corrispondente.

Se `<expression>` è vuoto o assente, la stringa di sostituzione viene aggiunta al percorso o alla query.

Se `<substitution>` è vuoto, la stringa o la sottostringa corrispondente viene rimossa. Se `<substitution>` non è specificato, il percorso o la stringa di query non vengono modificati.

>[!NOTE]
>
>Tutte le corrispondenze nella stringa di input vengono sostituite quando `replace="all"` è specificato nell’ `<rule>`,elemento a cui appartiene questo elemento `<substitution>`. Per impostazione predefinita, viene sostituita solo la prima corrispondenza con la stringa di sostituzione.

## Nota {#section-cedf2adabaaf441c9f598fb0ea180246}

La stringa di sostituzione non deve contenere caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<` oppure l&#39;intera stringa può essere racchiusa in una sezione CDATA XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
