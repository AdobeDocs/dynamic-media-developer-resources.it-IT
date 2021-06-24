---
description: Imposta qualsiasi attributo per un dato s7 elementID.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
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
