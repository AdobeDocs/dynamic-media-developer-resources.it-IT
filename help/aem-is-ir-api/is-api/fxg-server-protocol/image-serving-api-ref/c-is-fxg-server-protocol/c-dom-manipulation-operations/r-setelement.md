---
title: setElement
description: Imposta XML su un elementoID s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

Imposta XML su s7:elementID.

`setElement.elementID=<XML>`

Se per un elemento del nodo FXG è definito `s7:elementID`, il valore `<XML>` viene sostituito come elemento figlio. `<XML>` deve essere codificato.

## Esempio {#section-f23a998b18994dd3b5d4e1965718db9f}

Supponiamo che l&#39;attributo `s7:elementID="group2"` sia definito per un nodo `Group`, allora quanto segue è valido:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In questo esempio vengono rimossi tutti gli elementi figlio dal nodo `group2` e sostituiti con il nuovo nodo figlio `TextGraphic`.
