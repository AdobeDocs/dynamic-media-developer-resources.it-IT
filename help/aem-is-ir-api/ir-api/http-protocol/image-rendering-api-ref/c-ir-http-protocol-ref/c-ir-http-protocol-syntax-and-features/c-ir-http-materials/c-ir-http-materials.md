---
description: Il rendering delle immagini applica i materiali a gruppi o oggetti nelle vignettature.
seo-description: Il rendering delle immagini applica i materiali a gruppi o oggetti nelle vignettature.
seo-title: Materiali
solution: Experience Manager
title: Materiali
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Materiali{#materials}

Il rendering delle immagini applica i materiali a gruppi o oggetti nelle vignettature.

Un materiale è costituito da un insieme di *attributi*. Alcuni attributi sono richiesti per alcuni materiali, altri sono facoltativi e alcuni sono ignorati se presenti. Molti attributi hanno valori predefiniti. Non tutti i materiali possono essere applicati a tutti gli oggetti (ad es. un materiale mobile non può essere applicato a un divano).

Eventuali attributi che si verificano all&#39;interno di un segmento di specifica del materiale (MSS) ma non sono elencati sopra né nelle tabelle di materiale specifiche riportate di seguito vengono ignorati dal server.

Le tabelle seguenti elencano gli attributi del materiale di base. IR supporta attributi aggiuntivi per il controllo degli [effetti di rendering avanzati](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Salvo diversa indicazione, tutti gli attributi del materiale sono facoltativi, con valori predefiniti appropriati.

* [Colori solidi](r-ir-solid-colors.md)
* [Texture ripetibili](r-ir-repeatable-textures.md)
* [Bordi delle pareti](r-ir-wall-borders.md)
* [Decorazioni](r-ir-decals.md)
* [Scaffali](r-ir-cabinets.md)
* [Rivestimenti per finestre](r-ir-window-coverings.md)
