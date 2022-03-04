---
title: Materiali
description: Image Rendering applica materiali a gruppi o oggetti in vignette.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Materiali{#materials}

Image Rendering applica materiali a gruppi o oggetti in vignette.

Un materiale è costituito da un insieme di *attributes*. Alcuni attributi sono necessari per alcuni materiali, altri sono facoltativi e alcuni vengono ignorati se presenti. Molti attributi hanno valori predefiniti. Non tutti i materiali possono essere applicati a tutti gli oggetti (ad esempio, un materiale mobile non può essere applicato a un divano).

Gli attributi che si verificano all&#39;interno di un segmento di specifica del materiale (MSS) ma non sono elencati sopra o nelle specifiche tabelle del materiale riportate di seguito vengono ignorati dal server.

Nella tabella seguente sono elencati gli attributi di base dei materiali. IR supporta attributi aggiuntivi per il controllo [effetti di rendering avanzati](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Salvo diversa indicazione, tutti gli attributi del materiale sono facoltativi, con valori predefiniti appropriati.

* [Colori solidi](r-ir-solid-colors.md)
* [Trame ripetibili](r-ir-repeatable-textures.md)
* [Bordi a muro](r-ir-wall-borders.md)
* [Decorazioni](r-ir-decals.md)
* [Scaffali](r-ir-cabinets.md)
* [Rivestimenti per finestre](r-ir-window-coverings.md)
