---
description: Impostare il margine di rifilo. Imposta il margine di rifilo impostato nel file PDF.
seo-description: Impostare il margine di rifilo. Imposta il margine di rifilo impostato nel file PDF.
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
topic: Scene7 Image Serving - Image Rendering API
uuid: af94f9e8-a32e-439a-817a-a40aa8dc7dd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# trimMargin{#trimmargin}

Impostare il margine di rifilo. Imposta il margine di rifilo impostato nel file PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in punti

Per impostazione predefinita, `trimMargin` è impostato sulla dimensione completa del documento definita da `viewWidth` e `viewHeight`. I valori *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* vengono impostati automaticamente sul valore *[!DNL top]*, se non vengono specificati.
