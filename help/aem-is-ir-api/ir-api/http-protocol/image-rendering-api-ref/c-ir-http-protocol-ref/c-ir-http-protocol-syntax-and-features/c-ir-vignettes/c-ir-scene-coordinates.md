---
description: Lo spazio di coordinate della scena viene utilizzato per specificare le dimensioni e le distanze sulle superfici dell'oggetto texturable.
solution: Experience Manager
title: Coordinate della scena
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Coordinate della scena{#scene-coordinates}

Lo spazio di coordinate della scena viene utilizzato per specificare le dimensioni e le distanze sulle superfici dell&#39;oggetto texturable.

Poiché la maggior parte delle vignette sono scene reali che rappresentano oggetti fisici, la maggior parte delle vignette viene creata utilizzando pollici come unità per lo spazio di coordinate della scena. Possono essere utilizzate anche altre unità, come mm o cm. Image Rendering non supporta la conversione di unità.

I seguenti comandi accettano valori nello spazio di coordinate della scena:

* [grout=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [size=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
