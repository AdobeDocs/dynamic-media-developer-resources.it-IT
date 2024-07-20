---
title: pathEmbed
description: Incorpora i dati dei percorsi. Specifica se includere nell'immagine di risposta i percorsi Photoshop del file immagine di origine di livello 0.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Incorpora i dati dei percorsi. Specifica se includere nell&#39;immagine di risposta i percorsi Photoshop del file immagine di origine di livello 0.

`pathEmbed=0|1`

## Proprietà {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Attributo della richiesta. Ignorato se l’immagine di origine non contiene dati di percorsi. I dati dei percorsi vengono ridimensionati e ruotati come i dati dell’immagine. Vengono elaborati solo i percorsi dell&#39;immagine di origine di `layer=0`. I percorsi di altre immagini di livello vengono ignorati.

Ignorato se il formato dell&#39;immagine di output non supporta l&#39;incorporamento dei percorsi. Per un elenco dei formati immagine di output che supportano l&#39;incorporamento di percorsi, fare riferimento alla descrizione di `fmt=`.

## Restrizioni {#section-697cddb79a1542bc8457d2f4f59eec69}

Al momento, i percorsi aperti Photoshop (percorsi che non formano loop chiusi) non sono supportati per l’incorporamento nell’immagine di risposta.

## Predefinito {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, per nessuna incorporazione di percorsi nelle immagini di output.

## Consultate anche {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
