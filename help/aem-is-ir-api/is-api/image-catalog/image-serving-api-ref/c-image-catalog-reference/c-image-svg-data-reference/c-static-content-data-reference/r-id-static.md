---
description: ID
solution: Experience Manager
title: ID
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 5%

---

# ID{#id}

In genere, un identificatore breve e univoco, ad esempio un numero SKU, può avere un qualche tipo di suffisso, ad esempio se un SKU ha più immagini o ha varianti specifiche per le impostazioni internazionali. Può anche essere una stringa più complessa che assomiglia più a un percorso di file, per supportare una facile ristrutturazione di siti web con Image Serving.

>[!NOTE]
>
>Le tabelle immagine e SVG vengono unite in una singola tabella quando viene caricato il catalogo immagini. I valori ID devono essere univoci in entrambe le tabelle. Il record SVG viene scartato se la tabella di immagini contiene un record con lo stesso valore ID. Il contenuto statico è gestito con una tabella separata; gli elementi di contenuto statico e gli elementi immagine/SVG possono quindi avere gli stessi valori ID.

## Proprietà {#section-874a6853f67b4b229341ca76682884ae}

Stringa di testo. Obbligatorio. Identificatore del record per la tabella di dati immagine/SVG o contenuto statico. Ogni valore `catalog::Id` all&#39;interno di questo catalogo immagini/catalogo SVG o all&#39;interno di questo catalogo di contenuti statici deve essere univoco e non deve includere i caratteri &#39;,&#39;.

## Predefinito {#section-a26e7d83a5ee44b5918baef82ee48e14}

Nessuno.

## Consultate anche {#section-a258d818487d4ee6b7a99a65d18471a9}

[attributo::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
