---
title: Materiali
description: Image Rendering applica materiali a gruppi o oggetti nelle vignettature.
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

Image Rendering applica materiali a gruppi o oggetti nelle vignettature.

Un materiale è costituito da un insieme di *attributi*. Alcuni attributi sono necessari per alcuni materiali, altri sono facoltativi e altri vengono ignorati se presenti. Molti attributi hanno valori predefiniti. Non tutti i materiali possono essere applicati a tutti gli oggetti (ad esempio, un materiale di armadio non può essere applicato a un divano).

Tutti gli attributi che si verificano all&#39;interno di un segmento di specifica materiale (MSS, Material Specification Segment) ma non sono elencati sopra o nelle tabelle di materiale specifiche riportate di seguito vengono ignorati dal server.

Nelle tabelle seguenti sono elencati gli attributi dei materiali di base. IR supporta attributi aggiuntivi per il controllo [effetti di rendering avanzati](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Salvo diversa indicazione, tutti gli attributi dei materiali sono facoltativi, con valori di default appropriati.

* [Colori tinta unita](r-ir-solid-colors.md)
* [Texture ripetibili](r-ir-repeatable-textures.md)
* [Bordi muri](r-ir-wall-borders.md)
* [Decalcomania](r-ir-decals.md)
* [Archivi](r-ir-cabinets.md)
* [Rivestimenti per finestre](r-ir-window-coverings.md)
