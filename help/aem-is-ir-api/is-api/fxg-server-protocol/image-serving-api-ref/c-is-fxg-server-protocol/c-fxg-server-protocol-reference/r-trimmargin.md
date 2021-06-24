---
description: Imposta il margine di taglio. Imposta il margine di trim impostato nel file PDF.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# trimMargin{#trimmargin}

Imposta il margine di taglio. Imposta il margine di trim impostato nel file PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in punti

Per impostazione predefinita, il valore `trimMargin` è impostato sulle dimensioni complete del documento definito da `viewWidth` e `viewHeight`. I valori *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* vengono impostati automaticamente sul valore *[!DNL top]* se non specificato.
