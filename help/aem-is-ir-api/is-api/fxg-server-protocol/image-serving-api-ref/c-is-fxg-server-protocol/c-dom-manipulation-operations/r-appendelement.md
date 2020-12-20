---
description: Aggiungete XML a un ID di elemento s7.
seo-description: Aggiungete XML a un ID di elemento s7.
seo-title: appendElement
solution: Experience Manager
title: appendElement
topic: Scene7 Image Serving - Image Rendering API
uuid: 062c8288-4517-42a1-9f9f-f3c7bbb4b63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 1%

---


# appendElement{#appendelement}

Aggiungete XML a un ID di elemento s7.

`appendElement.elementID=<XML>`

Se un elemento nodo FXG ha una `s7:elementID` definita, il valore `<XML>` viene aggiunto come elemento secondario. È necessario codificare `<XML>`.

## Esempio {#section-4368570aa198485d91b73b4d0741478f}

Si supponga che per un nodo Gruppo sia definito un attributo `s7:elementID="group1"`, quindi è valido quanto segue:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In questo esempio viene aggiunto un elemento secondario dell&#39;elemento grafico di testo a `group1`.
