---
description: Incorpora i dati dei percorsi. Specifica se i percorsi Photoshop incorporati nella vignetta devono essere inclusi nell'immagine di risposta.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---


# pathEmbed{#pathembed}

Incorpora i dati dei percorsi. Specifica se i percorsi Photoshop incorporati nella vignetta devono essere inclusi nell&#39;immagine di risposta.

`pathEmbed=0|1`

## Proprietà {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Attributo di richiesta. Ignorato se la vignetta non contiene dati di percorsi. Se necessario, i dati dei percorsi vengono ridimensionati su `wid=` e/o `hei=` .

Ignorato se il formato immagine di output non supporta l’incorporazione del percorso. Fare riferimento alla descrizione di `fmt=` per un elenco dei formati immagine di output che supportano l&#39;incorporazione del percorso.

## Predefinito {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, per non incorporare percorsi nelle immagini di output.

## Consultate anche {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
