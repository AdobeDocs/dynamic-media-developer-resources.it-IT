---
description: Incorpora XMP metadati. Specifica se i metadati XMP devono essere inclusi nell'immagine di risposta.
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# xmpEmbed{#xmpembed}

Incorpora XMP metadati. Specifica se i metadati XMP devono essere inclusi nell&#39;immagine di risposta.

`xmpEmbed=0|1`

>[!NOTE]
>
>I dati XMP vengono passati dall&#39;immagine di origine all&#39;immagine di risposta senza modifiche. Questo potrebbe comportare l&#39;incorporazione di dati errati nell&#39;immagine di risposta.

## Proprietà {#section-27024c4272f44d9a8c264a0629193af2}

Attributo di richiesta. Ignorato se l’immagine di origine non contiene dati XMP. Vengono elaborati solo i dati XMP dall’immagine di origine di `layer=0`. I dati XMP provenienti da altre immagini di livello vengono ignorati.

Ignorato se il formato immagine di output non supporta XMP incorporazione. Fare riferimento alla descrizione di `fmt=` per un elenco dei formati immagine di output che supportano XMP incorporazione.

## Predefinito {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, per non incorporare percorsi nelle immagini di output.

## Consultate anche {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
