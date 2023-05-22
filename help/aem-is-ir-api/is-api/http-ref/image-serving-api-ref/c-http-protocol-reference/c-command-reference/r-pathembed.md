---
description: Incorpora i dati dei percorsi. Specifica se includere nell'immagine di risposta i percorsi Photoshop del file immagine di origine di livello 0.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Incorpora i dati dei percorsi. Specifica se includere nell&#39;immagine di risposta i percorsi Photoshop del file immagine di origine di livello 0.

`pathEmbed=0|1`

## Proprietà {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Attributo della richiesta. Ignorato se l’immagine di origine non contiene dati di percorsi. I dati dei percorsi vengono ridimensionati e ruotati come i dati dell’immagine. Solo percorsi dall’immagine sorgente di `layer=0` vengono elaborati; i tracciati provenienti da altre immagini di livello vengono ignorati.

Ignorato se il formato dell&#39;immagine di output non supporta l&#39;incorporamento dei percorsi. Fai riferimento alla descrizione di `fmt=` per un elenco dei formati di immagine di output che supportano l&#39;incorporamento dei percorsi.

## Restrizioni {#section-697cddb79a1542bc8457d2f4f59eec69}

Al momento, i percorsi aperti Photoshop (percorsi che non formano loop chiusi) non sono supportati per l’incorporamento nell’immagine di risposta.

## Predefinito {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, per non incorporare percorsi nelle immagini di output.

## Consultate anche {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
