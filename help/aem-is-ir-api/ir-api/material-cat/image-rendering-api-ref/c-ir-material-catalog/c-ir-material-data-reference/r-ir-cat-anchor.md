---
description: Ancoraggio immagine. Specifica il punto di ancoraggio (punto attivo) di una trama, un bordo di parete o un'immagine di decalcomania ripetibili.
solution: Experience Manager
title: Ancoraggio
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# Ancoraggio{#anchor}

Ancoraggio immagine. Specifica il punto di ancoraggio (punto attivo) di una trama, un bordo di parete o un&#39;immagine di decalcomania ripetibili.

Una texture ripetibile viene applicata a un oggetto vignettatura in modo che il punto di ancoraggio della texture si trovi nel punto di origine della texture dell&#39;oggetto. Un&#39;immagine di decalcomania viene applicata a un oggetto vignettatura in modo che il punto di ancoraggio della decalcomania si trovi nel punto di origine della decalcomania dell&#39;oggetto. Per i bordi delle pareti viene utilizzato solo il valore x, mentre il valore y viene ignorato.

## Proprietà {#section-bc4bc8b897c64535b88681e57d72942f}

Due numeri interi separati da una virgola. Offset pixel relativo all&#39;angolo superiore sinistro dell&#39;immagine. Ignorato se `catalog::Alignment=3` e dai materiali di colore e cabinet.

## Predefinito {#section-b7ccc419a356415294706cd295ae96c9}

Se il campo è vuoto o non presente, viene utilizzato l&#39;angolo superiore sinistro (0,0) dell&#39;immagine per i materiali di texture ripetibili o il centro dell&#39;immagine nel caso di materiali di decalcomania.

## Consultate anche {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalogo::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [ancoraggio=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
