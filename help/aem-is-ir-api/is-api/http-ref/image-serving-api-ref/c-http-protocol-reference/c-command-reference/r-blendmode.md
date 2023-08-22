---
title: blendMode
description: Metodo di fusione. Specifica il tipo di fusione utilizzato durante la composizione del livello. Simula i metodi di fusione comunemente utilizzati e disponibili in Photoshop. Per ulteriori informazioni, consulta la documentazione di Photoshop.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f0b8b0a-a8ac-4932-986c-5d14d3311f1b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 14%

---

# blendMode{#blendmode}

Metodo di fusione. Specifica il tipo di fusione utilizzato durante la composizione del livello. Simula i metodi di fusione comunemente utilizzati e disponibili in Photoshop. Per ulteriori informazioni, consulta la documentazione di Photoshop.

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
