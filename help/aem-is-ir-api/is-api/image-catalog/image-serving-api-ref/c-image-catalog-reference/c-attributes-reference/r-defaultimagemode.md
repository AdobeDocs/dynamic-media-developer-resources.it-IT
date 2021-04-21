---
description: Modalità immagine predefinita. Seleziona la modalità di applicazione dell’immagine predefinita quando le immagini specificate nella richiesta non vengono trovate.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# DefaultImageMode{#defaultimagemode}

Modalità immagine predefinita. Seleziona la modalità di applicazione dell’immagine predefinita quando le immagini specificate nella richiesta non vengono trovate.

## Proprietà {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. 0 per sostituire l&#39;intera immagine composita, anche se l&#39;immagine mancante è solo uno dei vari livelli; &#39;1&#39; per sostituire ogni immagine sorgente del livello mancante con l&#39;immagine predefinita e restituire il composito come di consueto.

## Restrizioni {#section-04cb0d50e8914564a8d226d0d4663c8b}

Image Serving ritorna a `DefaultImageMode=0` quando le richieste di rendering delle immagini nidificate, FXG o `req=set` non riescono.

## Predefinito {#section-9e318524a2a5496386901286748c7ee7}

Ereditato da `default::DefaultImage` se non definito o se vuoto.

## Consultate anche {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attributo::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
