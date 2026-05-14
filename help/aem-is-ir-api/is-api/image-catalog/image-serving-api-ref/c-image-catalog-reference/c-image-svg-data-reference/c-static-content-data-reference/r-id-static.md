---
title: ID
description: In genere, un identificatore breve e univoco, ad esempio un numero SKU, che può avere una sorta di suffisso, ad esempio se uno SKU ha più immagini o varianti specifiche per le impostazioni internazionali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
TQID: 'https://experienceleague.adobe.com/xPBbjaHO58J-4HFnChD1ybEVoE2AbRZuFVA8nbquEvg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 2%

---

# ID{#id}

In genere si tratta di un identificatore breve e univoco, ad esempio un numero SKU, che può avere una sorta di suffisso, ad esempio se uno SKU ha più immagini o varianti specifiche per le impostazioni internazionali. Può anche essere una stringa più complessa, più simile a un percorso di file, per supportare l’adattamento dei siti web tramite Image Server.

>[!NOTE]
>
>Le tabelle immagine e SVG vengono unite in un’unica tabella al caricamento del catalogo immagini. I valori ID devono essere univoci in entrambe le tabelle. Il record SVG viene eliminato se la tabella immagini contiene un record con lo stesso valore ID. Il contenuto statico viene gestito con una tabella separata; gli elementi di contenuto statico e gli elementi immagine/SVG possono quindi avere gli stessi valori ID.

## Proprietà {#section-874a6853f67b4b229341ca76682884ae}

Stringa di testo. Obbligatorio. Identificatore di record per la tabella di dati immagine/SVG o contenuto statico. Ogni valore `catalog::Id` in questo catalogo immagini/catalogo SVG o in questo catalogo di contenuti statici deve essere univoco e non deve includere i caratteri &quot;,&quot;.

## Predefinito {#section-a26e7d83a5ee44b5918baef82ee48e14}

Nessuno.

## Consultate anche {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
