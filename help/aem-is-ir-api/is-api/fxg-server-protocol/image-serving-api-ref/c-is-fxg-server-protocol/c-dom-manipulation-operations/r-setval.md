---
title: setVal
description: Imposta il valore del nodo di testo per s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---

# setVal{#setval}

Imposta il valore del nodo di testo per s7:elementID.

`setVal.elementID= *[!DNL value]*`

Se per un elemento del nodo FXG è definito un `s7:elementID`, è possibile modificare il valore di testo per tale nodo.

## Esempio {#section-f574fd66dedd4a219aa537d7bdabea23}

Supponiamo che l&#39;attributo `s7:elementID="paragraph1"` sia definito per un nodo `TextGraphic`, allora quanto segue è valido:

`&setVal.paragraph=Hello`

Questo esempio imposta il valore di testo per il nodo di paragrafo su &quot;Hello&quot;.
