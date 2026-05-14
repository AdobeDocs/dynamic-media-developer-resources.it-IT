---
title: op_sharpen
description: Immagini più nitide. Applica un filtro di nitidezza di base al livello o all'immagine di visualizzazione finale, dopo tutte le proporzioni, se layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
TQID: 'https://experienceleague.adobe.com/CLyNZKJir4mYZ2L04ZKpnkNk6LX9xs8VUwnwwPrs-Zc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
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

Compensate la leggera sfocatura causata dal ricampionamento dell&#39;immagine. Aumentiamo anche la qualità JPEG per evitare artefatti JPEG aggiuntivi lungo i bordi più nitidi.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Consultate anche {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
