---
description: Imposta margine di sanguinamento. Imposta il margine di pagina al vivo impostato nel file PDF.
solution: Experience Manager
title: margine
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# margine{#bleedmargin}

Imposta margine di sanguinamento. Imposta il margine di pagina al vivo impostato nel file PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in punti

Per impostazione predefinita, il valore `bleedMargin` è impostato sulle dimensioni complete del documento definito da `viewWidth` e `viewHeight`. I valori *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* vengono impostati automaticamente sul valore *[!DNL top]* se non specificato.
