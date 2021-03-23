---
description: Imposta il margine di taglio. Imposta il margine di trim impostato nel file PDF.
seo-description: Imposta il margine di taglio. Imposta il margine di trim impostato nel file PDF.
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
uuid: af94f9e8-a32e-439a-817a-a40aa8dc7dd4
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# trimMargin{#trimmargin}

Imposta il margine di taglio. Imposta il margine di trim impostato nel file PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in punti

Per impostazione predefinita, il valore `trimMargin` è impostato sulle dimensioni complete del documento definito da `viewWidth` e `viewHeight`. I valori *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* vengono impostati automaticamente sul valore *[!DNL top]* se non specificato.
