---
description: Ancoraggio immagine. Punto di origine quando l’immagine viene utilizzata come livello in un modello o in un’immagine composita.
seo-description: Ancoraggio immagine. Punto di origine quando l’immagine viene utilizzata come livello in un modello o in un’immagine composita.
seo-title: Ancoraggio
solution: Experience Manager
title: Ancoraggio
topic: Scene7 Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# Ancoraggio{#anchor}

Ancoraggio immagine. Punto di origine quando l’immagine viene utilizzata come livello in un modello o in un’immagine composita.

Definisce inoltre il punto centrale predefinito per la rotazione.

## Proprietà {#section-95740f14160744e7bc763094b8be40d8}

Due numeri interi, separati da una virgola. Offset dei pixel rispetto all’angolo superiore sinistro dell’immagine a risoluzione piena.

Sostituito da `anchor=`(che a sua volta può essere sostituito con `origin=`).

## Predefinito {#section-ca3a4cc837d643519eff15951f2b47a1}

Il punto centrale dell&#39;immagine viene utilizzato se il campo non è presente o se è vuoto e se si tratta di un record immagine valido (ovvero se `catalog::Path` è valido).

## Consultate anche {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
