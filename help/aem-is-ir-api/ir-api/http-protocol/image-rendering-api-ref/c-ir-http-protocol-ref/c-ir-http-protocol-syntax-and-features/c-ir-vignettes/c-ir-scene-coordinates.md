---
title: Coordinate scena
description: Lo spazio di coordinate della scena viene utilizzato per specificare le dimensioni e le distanze sulle superfici degli oggetti di texture.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# Coordinate scena{#scene-coordinates}

Lo spazio di coordinate della scena viene utilizzato per specificare le dimensioni e le distanze sulle superfici degli oggetti di texture.

Poiché la maggior parte delle vignettature sono scene reali che rappresentano oggetti fisici, la maggior parte delle vignettature viene creata utilizzando i pollici come unità per lo spazio di coordinate della scena. Possono essere utilizzate anche altre unità, come mm o cm. Image Rendering non supporta la conversione di unità.

I seguenti comandi accettano i valori nello spazio di coordinate della scena:

* [malta=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [size= dimensione](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
