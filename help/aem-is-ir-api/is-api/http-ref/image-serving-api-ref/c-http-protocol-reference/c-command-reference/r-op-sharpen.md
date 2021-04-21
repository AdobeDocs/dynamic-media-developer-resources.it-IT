---
description: Nitidezza immagine. Applica un filtro di nitidezza di base al livello o all'immagine di visualizzazione finale, dopo tutto il ridimensionamento, se layer=comp.
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---


# op_sharpen{#op-sharpen}

Nitidezza immagine. Applica un filtro di nitidezza di base al livello o all&#39;immagine di visualizzazione finale, dopo tutto il ridimensionamento, se layer=comp.

`op_sharpen=0|1`

Anche la maschera di livello o la maschera composita è affilata.

## Proprietà {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Attributo di livello o attributo di visualizzazione. Si applica al livello corrente o all&#39;immagine di visualizzazione finale se `layer=comp`. Ignorato dai livelli di effetto.

## Predefinito {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, senza effetto nitidezza.

## Esempio {#section-3202122df5db4e14b358ecabfb6d8b85}

Compensare la leggera sfocatura causata dal ricampionamento dell&#39;immagine. Aumentiamo anche la qualità JPEG per evitare ulteriori artefatti JPEG lungo i bordi più nitidi.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Consultate anche {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
