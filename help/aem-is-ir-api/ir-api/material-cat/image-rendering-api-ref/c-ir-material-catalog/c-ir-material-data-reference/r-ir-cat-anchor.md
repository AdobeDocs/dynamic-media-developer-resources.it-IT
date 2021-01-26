---
description: Ancoraggio immagine. Specifica il punto di ancoraggio (punto di attivazione) di una texture ripetibile, un bordo della parete o un'immagine decal.
seo-description: Ancoraggio immagine. Specifica il punto di ancoraggio (punto di attivazione) di una texture ripetibile, un bordo della parete o un'immagine decal.
seo-title: Ancoraggio
solution: Experience Manager
title: Ancoraggio
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---


# Ancoraggio{#anchor}

Ancoraggio immagine. Specifica il punto di ancoraggio (punto di attivazione) di una texture ripetibile, un bordo della parete o un&#39;immagine decal.

Una texture ripetibile viene applicata a un oggetto vignettatura in modo che il punto di ancoraggio della texture si trovi nel punto di origine della texture dell&#39;oggetto. Un&#39;immagine decal viene applicata a un oggetto vignettatura in modo che il punto di ancoraggio decal si trovi nel punto di origine decal dell&#39;oggetto. Per i bordi delle pareti, viene utilizzato solo il valore x; il valore y viene ignorato.

## Proprietà {#section-bc4bc8b897c64535b88681e57d72942f}

Due numeri interi, separati da una virgola. Offset dei pixel rispetto all’angolo superiore sinistro dell’immagine. Ignorato se `catalog::Alignment=3` e per colore in tinta unita e materiali di armadio.

## Predefinito {#section-b7ccc419a356415294706cd295ae96c9}

Se il campo è vuoto o non è presente, viene utilizzato l’angolo in alto a sinistra (0,0) dell’immagine per materiali di texture ripetibili, o il centro dell’immagine nel caso di materiali di decantazione.

## Consultate anche {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalogo::Allineamento](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [ancoraggio=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
