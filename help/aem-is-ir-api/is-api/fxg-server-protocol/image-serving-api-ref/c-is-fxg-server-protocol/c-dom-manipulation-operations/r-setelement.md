---
description: Impostate XML su un ID di elemento s7.
seo-description: Impostate XML su un ID di elemento s7.
seo-title: setElement
solution: Experience Manager
title: setElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setElement{#setelement}

Impostate XML su s7:elementID.

`setElement.elementID=<XML>`

Se un elemento nodo FXG ha una `s7:elementID` definizione, il `<XML>` valore viene sostituito come elemento secondario. The `<XML>` must be encoded.

## Esempio {#section-f23a998b18994dd3b5d4e1965718db9f}

Supponiamo che un `s7:elementID="group2"` attributo sia definito per un `Group` nodo e che quanto segue sia valido:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In questo esempio vengono rimossi tutti gli elementi secondari dal `group2`nodo e sostituiti con il nuovo nodo `TextGraphic` secondario.
