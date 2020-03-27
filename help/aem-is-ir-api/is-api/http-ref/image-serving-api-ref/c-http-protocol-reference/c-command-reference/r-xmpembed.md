---
description: Incorporare metadati XMP. Specifica se i metadati XMP devono essere inclusi nell'immagine di risposta.
seo-description: Incorporare metadati XMP. Specifica se i metadati XMP devono essere inclusi nell'immagine di risposta.
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# xmpEmbed{#xmpembed}

Incorporare metadati XMP. Specifica se i metadati XMP devono essere inclusi nell&#39;immagine di risposta.

`xmpEmbed=0|1`

>[!NOTE]
>
>I dati XMP vengono passati dall&#39;immagine di origine all&#39;immagine di risposta senza modifiche. Ciò potrebbe causare l&#39;incorporazione di dati non corretti nell&#39;immagine di risposta.

## Proprietà {#section-27024c4272f44d9a8c264a0629193af2}

Attributo di richiesta. Ignorato se l&#39;immagine di origine non contiene dati XMP. Vengono elaborati solo i dati XMP dell&#39;immagine di origine di `layer=0` . I dati XMP provenienti da altre immagini di livello vengono ignorati.

Ignorato se il formato dell&#39;immagine di output non supporta l&#39;incorporazione XMP. Fare riferimento alla descrizione di `fmt=` per un elenco dei formati immagine di output che supportano l&#39;incorporazione XMP.

## Predefinito {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, per non incorporare tracciati nelle immagini di output.

## Consultate anche {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
