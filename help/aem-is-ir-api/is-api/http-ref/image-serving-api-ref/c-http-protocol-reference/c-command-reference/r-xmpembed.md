---
title: xmpEmbed
description: Incorpora metadati XMP. Specifica se includere i metadati XMP nell'immagine di risposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

Incorpora metadati XMP. Specifica se includere i metadati XMP nell&#39;immagine di risposta.

`xmpEmbed=0|1`

>[!NOTE]
>
>I dati XMP vengono trasmessi dall’immagine sorgente all’immagine di risposta senza modifiche. Questo potrebbe causare l’incorporazione di dati errati nell’immagine di risposta.

## Proprietà {#section-27024c4272f44d9a8c264a0629193af2}

Attributo della richiesta. Ignorato se l’immagine di origine non contiene dati XMP. Solo i dati XMP dall’immagine sorgente di `layer=0` vengono elaborati. I dati XMP da altre immagini di livello vengono ignorati.

Ignorato se il formato dell&#39;immagine di output non supporta l&#39;incorporamento XMP. Fai riferimento alla descrizione di `fmt=` per un elenco dei formati di immagine di output che supportano l’incorporamento dell’XMP.

## Predefinito {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, per non incorporare percorsi nelle immagini di output.

## Consultate anche {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
