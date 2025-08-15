---
title: appendElement
description: Aggiungi XML a un elementoID s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f93bc31e-c0ae-4375-bb6a-eba6f11945b2
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 1%

---

# appendElement{#appendelement}

Aggiungi XML a s7:elementID.

`appendElement.elementID=<XML>`

Se per un elemento del nodo FXG è definito `s7:elementID`, il valore `<XML>` viene aggiunto come elemento figlio. `<XML>` deve essere codificato.

## Esempio {#section-4368570aa198485d91b73b4d0741478f}

Supponiamo che l&#39;attributo `s7:elementID="group1"` sia definito per un nodo di gruppo, allora quanto segue è valido:

`&appendElement.group1=<TextGraphic+fontFamily%3D"DefaultFont"+fontSize%3D"50"+x%3D"20"+y%3D"500" ><content><p><span>New+Text+Graphic+Tag+For+Demo<%2Fspan><%2Fp><%2Fcontent><%2FTextGraphic>`

In questo esempio un elemento figlio di un elemento grafico di testo viene aggiunto a `group1`.
