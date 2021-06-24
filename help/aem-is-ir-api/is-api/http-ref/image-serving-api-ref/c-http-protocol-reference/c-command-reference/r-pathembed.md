---
description: Incorpora i dati dei percorsi. Specifica se i percorsi Photoshop del file di immagine sorgente di livello 0 devono essere inclusi nell'immagine di risposta.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Incorpora i dati dei percorsi. Specifica se i percorsi Photoshop del file di immagine sorgente di livello 0 devono essere inclusi nell&#39;immagine di risposta.

`pathEmbed=0|1`

## Proprietà {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Attributo di richiesta. Ignorato se l’immagine di origine non contiene dati sui percorsi. I dati dei percorsi vengono ridimensionati e ruotati come i dati dell’immagine. Vengono elaborati solo i percorsi dell’immagine sorgente di `layer=0`; i percorsi di altre immagini di livello vengono ignorati.

Ignorato se il formato immagine di output non supporta l’incorporazione del percorso. Fare riferimento alla descrizione di `fmt=` per un elenco dei formati immagine di output che supportano l&#39;incorporazione del percorso.

## Restrizioni {#section-697cddb79a1542bc8457d2f4f59eec69}

I percorsi Photoshop aperti (percorsi che non formano loop chiusi) non sono supportati per l’incorporazione nell’immagine di risposta in questo momento.

## Predefinito {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, per non incorporare percorsi nelle immagini di output.

## Consultate anche {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
