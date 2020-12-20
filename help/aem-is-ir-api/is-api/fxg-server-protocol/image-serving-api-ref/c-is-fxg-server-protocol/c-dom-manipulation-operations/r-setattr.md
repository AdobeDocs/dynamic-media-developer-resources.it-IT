---
description: Impostate qualsiasi attributo per un ID di elemento s7 specificato.
seo-description: Impostate qualsiasi attributo per un ID di elemento s7 specificato.
seo-title: setAttr
solution: Experience Manager
title: setAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# setAttr{#setattr}

Impostate qualsiasi attributo per un ID di elemento s7 specificato.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Se un elemento nodo FXG ha una `s7:elementID` definita, potete manipolare gli attributi per tale nodo. Potete impostare tutte le coppie attributo/valore desiderate. Gli attributi non devono essere già definiti nel file FXG, ma devono essere validi per l’elemento node. Tutti i valori compresi tra `{}` devono essere eliminati.

## Esempio {#section-9c37470d5f0349e5b0a97291782cb7a6}

Si supponga che per un nodo `BitmapGraphic` sia definito un attributo `s7:elementID="Group1"`, quindi è valido quanto segue:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In questo esempio vengono impostati i valori *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* e *[!DNL scaleY]* per `BitmapGraphic` e vengono ignorati tutti i valori esistenti.
