---
title: Tipi di dati comuni
description: Gli attributi e i campi del catalogo possono contenere dati di uno dei seguenti tipi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Tipi di dati comuni{#common-data-types}

Gli attributi e i campi del catalogo possono contenere dati di uno dei seguenti tipi.

**Colore**

Valore colore. Valore RGB compresso esadecimale, facoltativamente preceduto da 0x. È possibile, ad esempio, specificare il valore RGB `128,255,0` come `0x80ff00` o `80ff00`.

**Contrassegno**

`0`=false, `1`=true; qualsiasi altro valore significa sconosciuto o non specificato.

**Enum**

`0` indica un valore sconosciuto o non specificato, come un campo vuoto. I valori validi `enum` sono numeri interi consecutivi, a partire da 1.

**Numero intero**

Valore intero firmato (ad esempio `0, -12, 34`). `0` o valori negativi possono avere un significato speciale.

**Numero reale**

Valore a virgola mobile firmato, ad esempio `0, 12.5, 245 , -2.34e4`. I valori 0 o negativi possono avere un significato particolare.

**Stringa di testo**

I delimitatori di stringa sono facoltativi, a meno che la stringa non contenga `<CR>`, `<LF>` o `<TAB>` caratteri. È possibile utilizzare come delimitatori virgolette singole e doppie. Se si utilizzano le virgolette, qualsiasi virgoletta incorporata nella stringa deve essere preceduta da due virgolette consecutive, ad esempio &#39;`This month''s Special`&#39;.
