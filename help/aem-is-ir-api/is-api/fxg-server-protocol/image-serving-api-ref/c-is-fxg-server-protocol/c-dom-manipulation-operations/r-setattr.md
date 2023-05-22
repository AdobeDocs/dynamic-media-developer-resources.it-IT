---
description: Imposta qualsiasi attributo per un determinato elementoID s7.
solution: Experience Manager
title: setAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# setAttr{#setattr}

Imposta qualsiasi attributo per un dato s7:elementID.

`setAttr.elementID={ *[!DNL attributeName]*= *[!DNL attributeValue]*, *[!DNL attributeName]*= *[!DNL AttributeValue]*…}`

Se un elemento del nodo FXG ha `s7:elementID` definito, puoi manipolare gli attributi di quel nodo. Puoi impostare tutte le coppie attributo/valore che desideri. Non è necessario che gli attributi siano già definiti nel file FXG, ma è necessario che siano validi per l’elemento nodo. Tutti i valori compresi tra `{}` deve essere scappato.

## Esempio {#section-9c37470d5f0349e5b0a97291782cb7a6}

Supponiamo che `s7:elementID="Group1"` attributo definito per un `BitmapGraphic` , è valido quanto segue:

`&setAttr.Group1={x=250%26y=170%26rotation=90%26scaleX=1%26scaleY=0.5}`

Questo esempio imposta *[!DNL x]*, *[!DNL y]*, *[!DNL rotation]*, *[!DNL scaleX]*, e *[!DNL scaleY]* per `BitmapGraphic` e sostituisce eventuali valori esistenti.
