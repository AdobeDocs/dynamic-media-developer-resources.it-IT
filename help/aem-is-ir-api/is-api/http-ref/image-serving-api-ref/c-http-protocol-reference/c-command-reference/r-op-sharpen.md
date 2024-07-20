---
title: op_sharpen
description: Immagini più nitide. Applica un filtro di nitidezza di base al livello o all'immagine di visualizzazione finale, dopo tutte le proporzioni, se layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# op_sharpen{#op-sharpen}

Immagini più nitide. Applica un filtro di nitidezza di base al livello o all&#39;immagine di visualizzazione finale, dopo tutte le proporzioni, se layer=comp.

`op_sharpen=0|1`

Anche la maschera di livello o la maschera composita viene resa più nitida.

## Proprietà {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Attributo di livello o attributo di visualizzazione. Si applica al livello corrente o all&#39;immagine di visualizzazione finale se `layer=comp`. Ignorato dai livelli degli effetti.

## Predefinito {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, senza alcun effetto di nitidezza.

## Esempio {#section-3202122df5db4e14b358ecabfb6d8b85}

Compensate la leggera sfocatura causata dal ricampionamento dell&#39;immagine. Aumentiamo anche la qualità delle JPEG per evitare artefatti JPEG aggiuntivi lungo i bordi affilati.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Consultate anche {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
