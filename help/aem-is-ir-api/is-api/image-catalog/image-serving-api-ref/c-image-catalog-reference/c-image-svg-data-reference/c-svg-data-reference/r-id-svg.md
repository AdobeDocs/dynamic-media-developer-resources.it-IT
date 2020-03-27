---
description: 'null'
seo-description: 'null'
seo-title: ID
solution: Experience Manager
title: ID
topic: Scene7 Image Serving - Image Rendering API
uuid: a700472c-e1eb-4eb0-95ff-7afd4ce27931
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# ID{#id}

In genere, un identificatore breve e univoco, ad esempio un numero SKU, può contenere un qualche tipo di suffisso, ad esempio se uno SKU ha più immagini o ha varianti specifiche per le impostazioni internazionali. Può trattarsi anche di una stringa più complessa, più simile al percorso di un file, per facilitare l’adattamento dei siti Web con Image Server.

>[!NOTE]
>
>Le tabelle immagine e SVG vengono unite in una singola tabella al caricamento del catalogo immagini. I valori ID devono essere univoci in entrambe le tabelle. Il record SVG viene scartato se la tabella di immagini contiene un record con lo stesso valore ID. Il contenuto statico è gestito con una tabella separata; gli elementi di contenuto statico e gli elementi immagine/SVG possono quindi avere gli stessi valori ID.

## Proprietà {#section-874a6853f67b4b229341ca76682884ae}

Stringa di testo. Obbligatorio. Identificatore del record per la tabella di dati immagine/SVG o di contenuto statico. Ogni `catalog::Id` valore presente nel catalogo immagini/catalogo SVG o nel catalogo di contenuti statici deve essere univoco e non deve includere caratteri &#39;,&#39;.

## Predefinito {#section-a26e7d83a5ee44b5918baef82ee48e14}

Nessuno.

## Consultate anche {#section-a258d818487d4ee6b7a99a65d18471a9}

[attributo::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
