---
description: Aggiungi XML a un elemento s7 elementID.
solution: Experience Manager
title: appendElement
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 1%

---

# appendElement{#appendelement}

Aggiungi XML a un s7:elementID.

`appendElement.elementID=<XML>`

Se un elemento nodo FXG ha un `s7:elementID` definito, il valore `<XML>` viene aggiunto come elemento figlio. È necessario codificare `<XML>`.

## Esempio {#section-4368570aa198485d91b73b4d0741478f}

Supponiamo che per un nodo Gruppo sia definito un attributo `s7:elementID="group1"` , quindi è valido quanto segue:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In questo esempio viene aggiunto un elemento figlio di un elemento grafico di testo a `group1`.
