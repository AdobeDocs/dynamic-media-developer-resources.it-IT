---
description: Elemento della stringa di sostituzione. Facoltativo negli elementi <rule> .
solution: Experience Manager
title: sostituzione
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 3%

---


# substitution{#substitution}

Elemento della stringa di sostituzione. Facoltativo negli elementi `<rule>`.

## Attributi {#section-d955eefc53eb4274861270669c01f9ca}

Nessuno.

## Dati {#section-a2688866ed6d41279a8478886e511ae3}

Stringa di sostituzione.

## Descrizione {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definisce una stringa sostitutiva per la stringa o sottostringa corrispondente nel percorso o nella query.

Se l&#39;espressione del pattern include espressioni secondarie (delimitate da parentesi), la prima stringa secondaria corrispondente viene sostituita dalla stringa di sostituzione. Se l&#39;espressione del pattern non include sottoespressioni, viene sostituita l&#39;intera stringa corrispondente.

Se `<expression>` è vuoto o assente, la stringa di sostituzione viene aggiunta al percorso o alla query.

Se `<substitution>` è vuoto, la stringa o la sottostringa corrispondente viene rimossa. Se `<substitution>` non è specificato, il percorso o la stringa di query non vengono modificati.

## Nota {#section-90fe89bb17a04804b7ff3c93df082892}

La stringa di sostituzione non deve contenere caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<` oppure l&#39;intera stringa può essere racchiusa in una sezione XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
