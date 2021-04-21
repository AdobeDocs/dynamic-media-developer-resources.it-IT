---
description: Impostare XML prima o dopo un nodo.
solution: Experience Manager
title: insertBefore,insertAfter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 1%

---


# insertBefore,insertAfter{#insertbefore-insertafter}

Impostare XML prima o dopo un nodo.

`insertBefore=<xml>, insertAfter=<xml>`

Se un elemento nodo FXG ha un `s7:elementID` definito, con questo comando possiamo aggiungere frammenti XML prima o dopo tale nodo.

## Esempio {#section-1fc8d4135ef94b60b838391e1568e70e}

Se disponiamo di un tag di gruppo come questo:

`<Group visible="true" s7:elementID="inner_shape">`

quindi:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

si traduce in:

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

si traduce in:

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
