---
description: Ancoraggio immagine Specifica il punto di ancoraggio (punto attivo) di una texture ripetibile, un bordo a parete o un'immagine decal.
solution: Experience Manager
title: Ancoraggio
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 3%

---


# Ancoraggio{#anchor}

Ancoraggio immagine Specifica il punto di ancoraggio (punto attivo) di una texture ripetibile, un bordo a parete o un&#39;immagine decal.

Una texture ripetibile viene applicata a un oggetto vignetta in modo che il punto di ancoraggio della texture si trovi nel punto di origine della texture dell&#39;oggetto. Un&#39;immagine decal viene applicata a un oggetto vignetta in modo che il punto di ancoraggio decal si trovi nel punto di origine decal dell&#39;oggetto. Per i bordi a parete, viene utilizzato solo il valore x; il valore y viene ignorato.

## Proprietà {#section-bc4bc8b897c64535b88681e57d72942f}

Due numeri interi, separati da una virgola. Offset pixel rispetto all&#39;angolo superiore sinistro dell&#39;immagine. Ignorato se `catalog::Alignment=3` e in base ai materiali a colori e a cabinet.

## Predefinito {#section-b7ccc419a356415294706cd295ae96c9}

Se il campo è vuoto o non è presente, viene utilizzato l&#39;angolo in alto a sinistra (0,0) dell&#39;immagine per materiali di texture ripetibili, o il centro dell&#39;immagine in caso di materiali di decal.

## Consultate anche {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalogo::Allineamento](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [ancoraggio=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
