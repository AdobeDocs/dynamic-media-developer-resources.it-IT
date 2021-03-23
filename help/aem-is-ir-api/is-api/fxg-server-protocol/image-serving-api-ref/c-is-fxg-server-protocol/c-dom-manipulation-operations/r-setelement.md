---
description: Imposta XML su un elementoID s7.
seo-description: Imposta XML su un elementoID s7.
seo-title: setElement
solution: Experience Manager
title: setElement
uuid: 717c9c3c-a2e0-4179-8158-9913f4e09a96
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# setElement{#setelement}

Imposta XML su s7:elementID.

`setElement.elementID=<XML>`

Se un elemento nodo FXG ha un `s7:elementID` definito, il valore `<XML>` viene sostituito come elemento figlio. È necessario codificare `<XML>`.

## Esempio {#section-f23a998b18994dd3b5d4e1965718db9f}

Supponiamo che per un nodo `Group` sia definito un attributo `s7:elementID="group2"` , quindi è valido quanto segue:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

Questo esempio rimuove tutti gli elementi secondari dal nodo `group2`e lo sostituisce con il nuovo nodo figlio `TextGraphic`.
