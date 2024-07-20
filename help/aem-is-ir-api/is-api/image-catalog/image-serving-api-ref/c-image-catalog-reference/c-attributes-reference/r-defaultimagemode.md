---
description: Modalità immagine predefinita. Seleziona la modalità di applicazione dell'immagine predefinita quando le immagini specificate nella richiesta non vengono trovate.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# DefaultImageMode{#defaultimagemode}

Modalità immagine predefinita. Seleziona la modalità di applicazione dell&#39;immagine predefinita quando le immagini specificate nella richiesta non vengono trovate.

## Proprietà {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. Fate clic su &#39;0&#39; per sostituire l&#39;intera immagine composita, anche se l&#39;immagine mancante è solo uno dei diversi livelli; su &#39;1&#39; per sostituire ogni immagine sorgente di livello mancante con l&#39;immagine predefinita e restituire l&#39;immagine composita come al solito.

## Restrizioni {#section-04cb0d50e8914564a8d226d0d4663c8b}

Image Server torna a `DefaultImageMode=0` se le richieste di Image Rendering, FXG o `req=set` nidificate non riescono.

## Predefinito {#section-9e318524a2a5496386901286748c7ee7}

Ereditato da `default::DefaultImage` se non definito o se vuoto.

## Consultate anche {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
