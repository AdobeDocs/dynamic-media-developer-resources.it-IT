---
description: Metodo di fusione. Specifica il tipo di fusione utilizzato quando il livello viene composto. Simula i metodi di fusione comunemente utilizzati disponibili in Photoshop. Per ulteriori informazioni, consultate la documentazione Photoshop.
seo-description: Metodo di fusione. Specifica il tipo di fusione utilizzato quando il livello viene composto. Simula i metodi di fusione comunemente utilizzati disponibili in Photoshop. Per ulteriori informazioni, consultate la documentazione Photoshop.
seo-title: blendMode
solution: Experience Manager
title: blendMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9ae30495-c10b-4c55-968e-effb602a0857
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 14%

---


# blendMode{#blendmode}

Metodo di fusione. Specifica il tipo di fusione utilizzato quando il livello viene composto. Simula i metodi di fusione comunemente utilizzati disponibili in Photoshop. Per ulteriori informazioni, consultate la documentazione Photoshop.

`blendMode=norm|dissolve|lighten|darken|mult|screen`

## Proprietà {#section-418aad5a417f49929d1953e226e5c8dd}

Attributo livello. Ignorato da `layer=0` e `layer=comp`.

## Predefinito {#section-69829acc6532448d8612a4a54e86f00e}

`blendMode=norm`

## Esempio {#section-d209dd9c270b469c87558a8910c50b61}

`…&size=200,200&bgColor=191,120,241&…`

`…&layer=1&src=myRootId/myImageId&opac=80&blendMode=dissolve&…`

## Consultate anche {#section-bc7ccdfcb310441c938c0bde3e00d7b3}

[opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5)
