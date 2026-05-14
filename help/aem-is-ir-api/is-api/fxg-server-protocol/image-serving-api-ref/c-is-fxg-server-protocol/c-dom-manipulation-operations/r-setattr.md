---
title: setAttr
description: Imposta qualsiasi attributo per un determinato elementoID s7.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4a51b97-ba5f-42a9-8d7b-8dc42ad5fe24
TQID: 'https://experienceleague.adobe.com/0O1uOLXsh-5PkBnXugpQYJHDAZep49WO3AA4hjClODk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
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
