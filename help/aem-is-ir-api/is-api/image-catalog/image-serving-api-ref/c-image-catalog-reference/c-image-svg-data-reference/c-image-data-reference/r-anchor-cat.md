---
description: Ancoraggio immagine Punto di origine quando l'immagine viene utilizzata come livello in un modello o immagine composita.
solution: Experience Manager
title: Ancoraggio
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 5%

---

# Ancoraggio{#anchor}

Ancoraggio immagine Punto di origine quando l&#39;immagine viene utilizzata come livello in un modello o immagine composita.

Definisce anche il punto centrale predefinito per la rotazione.

## Proprietà {#section-95740f14160744e7bc763094b8be40d8}

Due numeri interi, separati da una virgola. Offset pixel rispetto all&#39;angolo superiore sinistro dell&#39;immagine a risoluzione piena.

Sostituito da `anchor=`(che a sua volta può essere sostituito con `origin=`).

## Predefinito {#section-ca3a4cc837d643519eff15951f2b47a1}

Il punto centrale dell’immagine viene utilizzato se il campo non è presente o se è vuoto e se si tratta di un record immagine valido (ovvero se `catalog::Path` è valido).

## Consultate anche {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
