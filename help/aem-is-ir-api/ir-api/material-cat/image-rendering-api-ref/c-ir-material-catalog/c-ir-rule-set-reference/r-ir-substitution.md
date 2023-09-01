---
title: sostituzione
description: Elemento stringa di sostituzione. Opzionale in <rule> elementi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 2%

---

# sostituzione{#substitution}

Elemento stringa di sostituzione. Opzionale in `<rule>` elementi.

## Attributi {#section-d955eefc53eb4274861270669c01f9ca}

Nessuno.

## Dati {#section-a2688866ed6d41279a8478886e511ae3}

Stringa di sostituzione.

## Descrizione {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definisce una stringa sostitutiva per la stringa o la sottostringa corrispondente nel percorso o nella query.

Se l&#39;espressione del pattern include sottoespressioni (delimitate da parentesi), la prima sottostringa corrispondente viene sostituita con la stringa di sostituzione. Se l&#39;espressione di pattern non include sottoespressioni, viene sostituita l&#39;intera stringa corrispondente.

Se `<expression>` è vuoto o assente, la stringa di sostituzione viene aggiunta al percorso o alla query.

Se `<substitution>` è vuoto, la stringa o sottostringa corrispondente viene rimossa. Se `<substitution>` non è specificato, il percorso o la stringa di query non viene modificata.

## Nota {#section-90fe89bb17a04804b7ff3c93df082892}

La stringa di sostituzione non deve contenere caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati con `&` e `<`, rispettivamente, o l&#39;intera stringa può essere racchiusa in un XML `CDATA` sezione:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
