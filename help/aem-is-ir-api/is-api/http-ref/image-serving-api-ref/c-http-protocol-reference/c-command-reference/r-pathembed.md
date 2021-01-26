---
description: Incorpora i dati dei percorsi. Specifica se i percorsi Photoshop del file di immagine sorgente del livello 0 devono essere inclusi nell’immagine di risposta.
seo-description: Incorpora i dati dei percorsi. Specifica se i percorsi Photoshop del file di immagine sorgente del livello 0 devono essere inclusi nell’immagine di risposta.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# pathEmbed{#pathembed}

Incorpora i dati dei percorsi. Specifica se i percorsi Photoshop del file di immagine sorgente del livello 0 devono essere inclusi nell’immagine di risposta.

`pathEmbed=0|1`

## Proprietà {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Attributo di richiesta. Ignorato se l&#39;immagine di origine non contiene dati sui percorsi. I dati dei percorsi vengono ridimensionati e ruotati come i dati immagine. Vengono elaborati solo i percorsi dall&#39;immagine di origine di `layer=0`; i percorsi di altre immagini di livello vengono ignorati.

Ignorato se il formato dell&#39;immagine di output non supporta l&#39;incorporazione del percorso. Fare riferimento alla descrizione di `fmt=` per un elenco dei formati di immagine di output che supportano l&#39;incorporamento dei percorsi.

## Restrizioni {#section-697cddb79a1542bc8457d2f4f59eec69}

Al momento, i percorsi Photoshop aperti (percorsi che non formano loop chiusi) non sono supportati per l&#39;incorporamento nell&#39;immagine di risposta.

## Predefinito {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, per non incorporare tracciati nelle immagini di output.

## Consultate anche {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
