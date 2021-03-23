---
description: Imposta margine di sanguinamento. Imposta il margine di pagina al vivo impostato nel file PDF.
seo-description: Imposta margine di sanguinamento. Imposta il margine di pagina al vivo impostato nel file PDF.
seo-title: margine
solution: Experience Manager
title: margine
uuid: 084d09dd-3f8e-4d2b-8a1c-21d87d925b14
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# bleedmargin{#bleedmargin}

Imposta margine di sanguinamento. Imposta il margine di pagina al vivo impostato nel file PDF.

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in punti

Per impostazione predefinita, il valore `bleedMargin` è impostato sulle dimensioni complete del documento definito da `viewWidth` e `viewHeight`. I valori *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* vengono impostati automaticamente sul valore *[!DNL top]* se non specificato.
