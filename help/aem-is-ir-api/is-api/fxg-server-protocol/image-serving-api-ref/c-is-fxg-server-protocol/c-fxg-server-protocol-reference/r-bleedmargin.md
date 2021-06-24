---
description: Imposta margine di sanguinamento. Imposta il margine di pagina al vivo impostato nel file PDF.
solution: Experience Manager
title: margine
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# margine{#bleedmargin}

Imposta margine di sanguinamento. Imposta il margine di pagina al vivo impostato nel file PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in punti

Per impostazione predefinita, il valore `bleedMargin` è impostato sulle dimensioni complete del documento definito da `viewWidth` e `viewHeight`. I valori *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* vengono impostati automaticamente sul valore *[!DNL top]* se non specificato.
