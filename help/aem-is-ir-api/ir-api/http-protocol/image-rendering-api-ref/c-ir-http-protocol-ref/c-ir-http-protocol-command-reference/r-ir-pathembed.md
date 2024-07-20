---
title: pathEmbed
description: Incorpora i dati dei percorsi. Specifica se includere nell'immagine di risposta i percorsi Photoshop incorporati nella vignettatura.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# pathEmbed{#pathembed}

Incorpora i dati dei percorsi. Specifica se includere nell&#39;immagine di risposta i percorsi Photoshop incorporati nella vignettatura.

`pathEmbed=0|1`

## Proprietà {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Attributo della richiesta. Ignorato se la vignettatura non contiene dati di percorsi. Se necessario, i dati dei percorsi vengono ridimensionati a `wid=` e/o `hei=`.

Ignorato se il formato dell&#39;immagine di output non supporta l&#39;incorporamento dei percorsi. Per un elenco dei formati immagine di output che supportano l&#39;incorporamento di percorsi, fare riferimento alla descrizione di `fmt=`.

## Predefinito {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, per nessuna incorporazione di percorsi nelle immagini di output.

## Consultate anche {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
