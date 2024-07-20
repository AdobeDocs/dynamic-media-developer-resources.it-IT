---
title: setAttr
description: Imposta qualsiasi attributo per un determinato elementoID s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

Imposta qualsiasi attributo per un dato s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Se per un elemento del nodo FXG è definito un `s7:elementID`, è possibile modificare gli attributi per tale nodo. Puoi impostare tutte le coppie attributo/valore che desideri. Non è necessario che gli attributi siano già definiti nel file FXG, ma è necessario che siano validi per l’elemento nodo. Tutti i valori compresi tra `{}` devono essere con escape.

## Esempio {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supponiamo che l&#39;attributo `s7:elementID="Group1"` sia definito per un nodo `BitmapGraphic`, allora quanto segue è valido:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

In questo esempio vengono impostati *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]* e *[!DNL scaleY]* per `BitmapGraphic` e vengono ignorati tutti i valori esistenti.
