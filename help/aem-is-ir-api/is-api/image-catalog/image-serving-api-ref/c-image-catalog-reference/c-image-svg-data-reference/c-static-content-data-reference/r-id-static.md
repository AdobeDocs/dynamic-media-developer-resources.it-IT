---
title: ID
description: In genere, un identificatore breve e univoco, ad esempio un numero SKU, che può avere una sorta di suffisso, ad esempio se uno SKU ha più immagini o varianti specifiche per le impostazioni internazionali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 1%

---

# ID{#id}

In genere si tratta di un identificatore breve e univoco, ad esempio un numero SKU, che può avere una sorta di suffisso, ad esempio se uno SKU ha più immagini o varianti specifiche per le impostazioni internazionali. Può anche essere una stringa più complessa, più simile a un percorso di file, per supportare l’adattamento dei siti web tramite Image Server.

>[!NOTE]
>
>Le tabelle immagine e SVG vengono unite in un’unica tabella al caricamento del catalogo immagini. I valori ID devono essere univoci in entrambe le tabelle. Il record SVG viene eliminato se la tabella immagini contiene un record con lo stesso valore ID. Il contenuto statico viene gestito con una tabella separata; gli elementi di contenuto statico e gli elementi immagine/SVG possono quindi avere gli stessi valori ID.

## Proprietà {#section-874a6853f67b4b229341ca76682884ae}

Stringa di testo. Obbligatorio. Identificatore di record per la tabella di dati immagine/SVG o contenuto statico. Ogni valore `catalog::Id` in questo catalogo immagini/catalogo SVG o in questo catalogo contenuti statico deve essere univoco e non deve includere i caratteri &quot;,&quot;.

## Predefinito {#section-a26e7d83a5ee44b5918baef82ee48e14}

Nessuno.

## Consultate anche {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
