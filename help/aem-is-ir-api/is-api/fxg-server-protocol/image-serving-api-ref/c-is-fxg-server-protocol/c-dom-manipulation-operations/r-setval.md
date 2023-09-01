---
title: setVal
description: Imposta il valore del nodo di testo per s7 elementID.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---

# setVal{#setval}

Imposta il valore del nodo di testo per s7:elementID.

`setVal.elementID= *[!DNL value]*`

Se un elemento del nodo FXG ha `s7:elementID` definito, il valore di testo per tale nodo può essere manipolato.

## Esempio {#section-f574fd66dedd4a219aa537d7bdabea23}

Supponiamo che `s7:elementID="paragraph1"` attributo definito per un `TextGraphic` nodo, è valido quanto segue:

`&setVal.paragraph=Hello`

Questo esempio imposta il valore di testo per il nodo di paragrafo su &quot;Hello&quot;.
