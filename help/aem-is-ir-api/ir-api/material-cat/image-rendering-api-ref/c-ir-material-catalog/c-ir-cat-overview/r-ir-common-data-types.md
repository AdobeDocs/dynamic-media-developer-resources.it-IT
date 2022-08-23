---
title: Tipi di dati comuni
description: Gli attributi e i campi del catalogo possono contenere dati di uno dei seguenti tipi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Tipi di dati comuni{#common-data-types}

Gli attributi e i campi del catalogo possono contenere dati di uno dei seguenti tipi.

**Colore**

Valore del colore. Valore RGB esadecimale compresso, eventualmente preceduto da 0x. Ad esempio, il valore RGB `128,255,0` può essere specificato come `0x80ff00` o `80ff00`.

**Flag**

`0`=false; `1`=true; qualsiasi altro valore significa sconosciuto o non specificato.

**Enum**

`0` indica un valore sconosciuto o non specificato, come un campo vuoto. Valido `enum` i valori sono numeri interi consecutivi, a partire da 1.

**Numero intero**

Valore intero firmato (ad esempio `0, -12, 34`). `0` o valori negativi possono avere un significato speciale.

**Numero reale**

Valore a virgola mobile firmato (ad esempio, `0, 12.5, 245 , -2.34e4`). 0 o valori negativi possono avere un significato speciale.

**Stringa di testo**

I delimitatori di stringa sono facoltativi, a meno che la stringa non contenga `<CR>`, `<LF>`oppure `<TAB>` caratteri. Le virgolette singole e doppie possono essere utilizzate come delimitatori. Se vengono utilizzate le virgolette, tutte le virgolette incorporate nella stringa devono essere precedute da due virgolette consecutive (ad esempio, &#39; `This month''s Special`&quot;).
