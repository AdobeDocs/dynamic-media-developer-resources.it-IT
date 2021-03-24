---
description: Imposta il valore del nodo di testo per s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

Imposta il valore del nodo di testo per s7:elementID.

`setVal.elementID= *[!DNL value]*`

Se un elemento del nodo FXG ha una `s7:elementID` definita, il valore del testo per quel nodo può essere manipolato.

## Esempio {#section-f574fd66dedd4a219aa537d7bdabea23}

Supponiamo che per un nodo `TextGraphic` sia definito un attributo `s7:elementID="paragraph1"` , quindi è valido quanto segue:

`&setVal.paragraph=Hello`

In questo esempio il valore del testo per il nodo paragrafo viene impostato su &quot;Hello&quot;.
