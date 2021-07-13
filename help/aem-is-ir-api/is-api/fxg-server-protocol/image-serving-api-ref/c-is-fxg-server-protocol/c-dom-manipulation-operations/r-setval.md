---
description: Imposta il valore del nodo di testo per s7 elementID.
solution: Experience Manager
title: setVal
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 03ec2ffb-ad9a-4135-bc31-2d71284955f6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
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
