---
description: Gli attributi e i campi del catalogo possono contenere dati di uno dei seguenti tipi.
seo-description: Gli attributi e i campi del catalogo possono contenere dati di uno dei seguenti tipi.
seo-title: Tipi di dati comuni
solution: Experience Manager
title: Tipi di dati comuni
topic: Scene7 Image Serving - Image Rendering API
uuid: b36cf09d-dee2-4e8b-9500-e8fa4c5c112f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tipi di dati comuni{#common-data-types}

Gli attributi e i campi del catalogo possono contenere dati di uno dei seguenti tipi.

**Colore**

Valore colore. Valore RGB esadecimale compresso, facoltativamente preceduto da 0x. Ad esempio, il valore RGB `128,255,0` può essere specificato come `0x80ff00` o `80ff00`.

**Flag**

`0`=false, `1`=true; qualsiasi altro valore indica sconosciuto o non specificato.

**Enum**

0 indica un valore sconosciuto o non specificato, come un campo vuoto. I `enum` valori validi sono numeri interi consecutivi, a partire da 1.

**Numero intero**

Valore intero con segno (ad esempio 0, -12, 34). 0 o valori negativi possono avere un significato speciale.

**Numero reale**

Valore a virgola mobile con firma (ad esempio `0, 12.5, 245 , -2.34e4`). 0 o valori negativi possono avere un significato speciale.

**Stringa di testo**

I delimitatori di stringa sono facoltativi, a meno che la stringa non contenga `<CR>`, `<LF>`o `<TAB>` caratteri. È possibile utilizzare come delimitatori sia le virgolette singole che doppie. Se vengono utilizzate le virgolette, queste devono essere racchiuse all&#39;interno della stringa utilizzando due virgolette consecutive (ad es. &#39; `This month''s Special`&#39;).
