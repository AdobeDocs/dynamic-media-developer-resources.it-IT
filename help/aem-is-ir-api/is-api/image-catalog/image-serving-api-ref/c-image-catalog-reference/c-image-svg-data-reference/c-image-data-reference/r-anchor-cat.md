---
description: Ancoraggio immagine. Punto di origine quando questa immagine viene utilizzata come livello in un modello o in un'immagine composita.
solution: Experience Manager
title: Ancoraggio
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# Ancoraggio{#anchor}

Ancoraggio immagine. Punto di origine quando questa immagine viene utilizzata come livello in un modello o in un&#39;immagine composita.

Definisce anche il punto centrale di default per la rotazione.

## Proprietà {#section-95740f14160744e7bc763094b8be40d8}

Due numeri interi separati da una virgola. Offset pixel relativo all&#39;angolo superiore sinistro dell&#39;immagine a risoluzione massima.

Sostituito da `anchor=`(che a sua volta può essere ignorato con `origin=`).

## Predefinito {#section-ca3a4cc837d643519eff15951f2b47a1}

Il punto centrale dell’immagine viene utilizzato se questo campo non è presente o se è vuoto e se si tratta di un record immagine valido (ad esempio se `catalog::Path` è valido).

## Consultate anche {#section-f605d29c3f5d48ad8e2a374f11886f19}

[ancoraggio=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin= origine](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
