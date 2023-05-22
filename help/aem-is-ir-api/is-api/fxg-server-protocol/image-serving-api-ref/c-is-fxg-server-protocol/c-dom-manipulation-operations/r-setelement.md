---
description: Imposta XML su un elementoID s7.
solution: Experience Manager
title: setElement
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 979e6070-6e24-4caf-9d87-2c80b734c996
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# setElement{#setelement}

Imposta XML su s7:elementID.

`setElement.elementID=<XML>`

Se un elemento del nodo FXG ha `s7:elementID` definito, il `<XML>` Il valore viene sostituito come elemento figlio. Il `<XML>` deve essere codificato.

## Esempio {#section-f23a998b18994dd3b5d4e1965718db9f}

Supponiamo che `s7:elementID="group2"` attributo definito per un `Group` nodo, è valido quanto segue:

`&setElement.group2=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500"><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In questo esempio vengono rimossi tutti gli elementi figlio dal `group2`e lo sostituisce con un nuovo `TextGraphic` nodo figlio.
