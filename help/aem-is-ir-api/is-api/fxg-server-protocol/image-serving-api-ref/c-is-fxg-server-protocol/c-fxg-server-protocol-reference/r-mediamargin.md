---
description: Impostare il margine del supporto. Imposta il margine del supporto impostato nel file PDF.
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

Impostare il margine del supporto. Imposta il margine del supporto impostato nel file PDF.

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` in punti

Per impostazione predefinita, il valore `mediaMargin` è impostato sulle dimensioni complete del documento definito da `viewWidth` e `viewHeight`. I valori *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* vengono impostati automaticamente sul valore *[!DNL top]* se non specificato.
