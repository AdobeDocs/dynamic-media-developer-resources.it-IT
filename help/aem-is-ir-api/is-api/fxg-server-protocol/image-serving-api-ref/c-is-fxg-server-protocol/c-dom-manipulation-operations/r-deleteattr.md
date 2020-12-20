---
description: Eliminate qualsiasi attributo per un ID di elemento s7 specificato.
seo-description: Eliminate qualsiasi attributo per un ID di elemento s7 specificato.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

Eliminate qualsiasi attributo per un ID di elemento s7 specificato.

`deleteAttr.elementID={attributeName%26attributeName}`

Se un elemento nodo FXG ha una `s7:elementID` definita, gli attributi per tale nodo possono essere eliminati con questo comando.

## Esempio {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Questo esempio rimuove gli attributi *[!DNL x]*, *[!DNL y]* e *[!DNL visible]* dal nodo FXG originale.
