---
title: sostituzione
description: Elemento stringa di sostituzione. Facoltativo negli elementi <rule>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
TQID: 'https://experienceleague.adobe.com/GqJBLso7oigoeCJ-0KQzFv2aeoAiVzumjlDTtjBSDI4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 1%

---

# sostituzione{#substitution}

Elemento stringa di sostituzione. Facoltativo negli elementi `<rule>`.

## Attributi {#section-d955eefc53eb4274861270669c01f9ca}

Nessuno.

## Dati {#section-a2688866ed6d41279a8478886e511ae3}

Stringa di sostituzione.

## Descrizione {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Definisce una stringa sostitutiva per la stringa o la sottostringa corrispondente nel percorso o nella query.

Se l&#39;espressione del pattern include sottoespressioni (delimitate da parentesi), la prima sottostringa corrispondente viene sostituita con la stringa di sostituzione. Se l&#39;espressione di pattern non include sottoespressioni, viene sostituita l&#39;intera stringa corrispondente.

Se `<expression>` è vuoto o assente, la stringa di sostituzione viene aggiunta al percorso o alla query.

Se `<substitution>` è vuoto, la stringa o sottostringa corrispondente viene rimossa. Se `<substitution>` non è specificato, il percorso o la stringa di query non verrà modificata.

## Nota {#section-90fe89bb17a04804b7ff3c93df082892}

La stringa di sostituzione non deve contenere caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<` oppure l&#39;intera stringa può essere racchiusa in una sezione XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
