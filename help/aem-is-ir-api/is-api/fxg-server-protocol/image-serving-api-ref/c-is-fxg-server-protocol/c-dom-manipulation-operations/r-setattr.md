---
description: Imposta qualsiasi attributo per un dato s7 elementID.
seo-description: Imposta qualsiasi attributo per un dato s7 elementID.
seo-title: setAttr
solution: Experience Manager
title: setAttr
uuid: 968f7496-3cd4-4670-96fc-53127bba9a83
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# setAttr{#setattr}

Imposta qualsiasi attributo per un dato s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Se un elemento nodo FXG ha una `s7:elementID` definita, puoi manipolare gli attributi per quel nodo. Puoi impostare tutte le coppie attributo/valore desiderate. Gli attributi non devono essere già definiti nell&#39;FXG, ma devono essere validi per l&#39;elemento node. Tutti i valori compresi tra `{}` devono essere escape.

## Esempio {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supponiamo che per un nodo `BitmapGraphic` sia definito un attributo `s7:elementID="Group1"` , quindi è valido quanto segue:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Questo esempio imposta i valori *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* e *[!DNL scaleY]* per `BitmapGraphic` e sostituisce eventuali valori esistenti.
