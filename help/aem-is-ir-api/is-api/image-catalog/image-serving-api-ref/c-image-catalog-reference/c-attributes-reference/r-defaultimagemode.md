---
description: Modalità immagine predefinita. Seleziona l’applicazione dell’immagine predefinita quando le immagini specificate nella richiesta non vengono trovate.
seo-description: Modalità immagine predefinita. Seleziona l’applicazione dell’immagine predefinita quando le immagini specificate nella richiesta non vengono trovate.
seo-title: DefaultImageMode
solution: Experience Manager
title: DefaultImageMode
topic: Scene7 Image Serving - Image Rendering API
uuid: e5640f09-e1e3-473b-8fbc-84c6bfce2460
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# DefaultImageMode{#defaultimagemode}

Modalità immagine predefinita. Seleziona l’applicazione dell’immagine predefinita quando le immagini specificate nella richiesta non vengono trovate.

## Proprietà {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &#39;0&#39; per sostituire l&#39;intera immagine composita, anche se l&#39;immagine mancante è solo uno dei vari livelli; &#39;1&#39; per sostituire ogni immagine sorgente del livello mancante con l&#39;immagine predefinita e restituire il composito come di consueto.

## Restrizioni {#section-04cb0d50e8914564a8d226d0d4663c8b}

Image Serving torna a `DefaultImageMode=0` quando le richieste di rendering delle immagini nidificate, FXG o `req=set` hanno esito negativo.

## Predefinito {#section-9e318524a2a5496386901286748c7ee7}

Ereditato da `default::DefaultImage` se non definito o se vuoto.

## Consultate anche {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
