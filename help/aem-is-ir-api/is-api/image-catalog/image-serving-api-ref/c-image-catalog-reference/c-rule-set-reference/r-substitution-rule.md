---
description: Elemento stringa di sostituzione. Facoltativo negli elementi <rule>.
solution: Experience Manager
title: sostituzione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
TQID: 'https://experienceleague.adobe.com/ZdC23CxEXKYN0d-h7nM8588KTS5Vy6BTh0kl5Iseq0w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
ht-degree: 1%

---

# sostituzione{#substitution}

Elemento stringa di sostituzione. Facoltativo negli elementi `<rule>`.

## Attributi {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Nessuno.

## Dati {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Stringa di sostituzione.

## Descrizione {#section-4a64a93f5e1a4d04a2db19166578bf76}

Definisce una stringa sostitutiva per la stringa o la sottostringa corrispondente nel percorso o nella query.

Se l&#39;espressione del pattern include sottoespressioni (delimitate da parentesi), la prima sottostringa corrispondente viene sostituita con la stringa di sostituzione. Se l’espressione del pattern non include sottoespressioni, viene sostituita l’intera stringa corrispondente.

Se `<expression>` è vuoto o assente, la stringa di sostituzione viene aggiunta al percorso o alla query.

Se `<substitution>` è vuoto, la stringa o sottostringa corrispondente viene rimossa. Se `<substitution>` non è specificato, il percorso o la stringa di query non verrà modificata.

>[!NOTE]
>
>Tutte le corrispondenze nella stringa di input vengono sostituite quando `replace="all"` è specificato nell&#39;elemento `<rule>`, a cui appartiene questo elemento `<substitution>`. Per impostazione predefinita, solo la prima corrispondenza viene sostituita con la stringa di sostituzione.

## Nota {#section-cedf2adabaaf441c9f598fb0ea180246}

La stringa di sostituzione non deve contenere caratteri letterali &lt; e &amp;. Questi caratteri riservati possono essere codificati rispettivamente con `&` e `<` oppure l&#39;intera stringa può essere racchiusa in una sezione XML CDATA:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
