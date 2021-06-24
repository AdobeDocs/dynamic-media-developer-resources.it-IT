---
description: Elimina qualsiasi attributo per un dato s7 elementID.
solution: Experience Manager
title: deleteAttr
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 7cecd0aa-c928-4652-a92f-f21ebcf83304
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 1%

---

# deleteAttr{#deleteattr}

Elimina qualsiasi attributo per un dato s7:elementID.

`deleteAttr.elementID={attributeName%26attributeName}`

Se un elemento nodo FXG ha un `s7:elementID` definito, gli attributi per quel nodo possono essere eliminati con questo comando.

## Esempio {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

Questo esempio rimuove gli attributi *[!DNL x]*, *[!DNL y]* e *[!DNL visible]* dal nodo FXG originale.
