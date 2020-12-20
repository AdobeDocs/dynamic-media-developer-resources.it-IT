---
description: Impostate il valore del nodo di testo per l’ID di elemento s7.
seo-description: Impostate il valore del nodo di testo per l’ID di elemento s7.
seo-title: setVal
solution: Experience Manager
title: setVal
topic: Scene7 Image Serving - Image Rendering API
uuid: 27ced070-6434-477d-aacf-053d53ee58ff
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 1%

---


# setVal{#setval}

Impostate il valore del nodo di testo per s7:elementID.

`setVal.elementID= *[!DNL value]*`

Se un elemento nodo FXG ha una `s7:elementID` definita, il valore del testo per tale nodo può essere manipolato.

## Esempio {#section-f574fd66dedd4a219aa537d7bdabea23}

Si supponga che per un nodo `TextGraphic` sia definito un attributo `s7:elementID="paragraph1"`, quindi è valido quanto segue:

`&setVal.paragraph=Hello`

In questo esempio il valore del testo per il nodo paragrafo viene impostato su &quot;Hello&quot;.
